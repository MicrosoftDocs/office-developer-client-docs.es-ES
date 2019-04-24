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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279531"
---
# <a name="iprovideradmingetprovidertable"></a><span data-ttu-id="185fb-103">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="185fb-103">IProviderAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="185fb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="185fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="185fb-105">Proporciona acceso a la tabla de proveedores del servicio de mensajes, una lista de los proveedores de servicios del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="185fb-105">Provides access to the message service's provider table, a list of the service providers in the message service.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="185fb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="185fb-106">Parameters</span></span>

 <span data-ttu-id="185fb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="185fb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="185fb-108">a Máscara de máscara de marcadores que controla el tipo de las cadenas devueltas en las columnas de la tabla del proveedor.</span><span class="sxs-lookup"><span data-stu-id="185fb-108">[in] A bitmask of flags that controls the type of the strings returned in the provider table's columns.</span></span> <span data-ttu-id="185fb-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="185fb-109">The following flag can be set:</span></span>
    
<span data-ttu-id="185fb-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="185fb-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="185fb-111">Las columnas de cadena están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="185fb-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="185fb-112">Si no se establece la marca MAPI_UNICODE, las columnas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="185fb-112">If the MAPI_UNICODE flag is not set, the columns are in ANSI format.</span></span>
    
 <span data-ttu-id="185fb-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="185fb-113">_lppTable_</span></span>
  
> <span data-ttu-id="185fb-114">contempla Un puntero a un puntero a la tabla del proveedor.</span><span class="sxs-lookup"><span data-stu-id="185fb-114">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="185fb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="185fb-115">Return value</span></span>

<span data-ttu-id="185fb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="185fb-116">S_OK</span></span> 
  
> <span data-ttu-id="185fb-117">La tabla de proveedores se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="185fb-117">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="185fb-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="185fb-118">Remarks</span></span>

<span data-ttu-id="185fb-119">El método **IProviderAdmin:: GetProviderTable** recupera un puntero a la tabla de proveedores del servicio de mensajes, una tabla que mantiene MAPI que contiene información acerca de cada proveedor de servicios en el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="185fb-119">The **IProviderAdmin::GetProviderTable** method retrieves a pointer to the message service's provider table, a table that MAPI maintains that contains information about each service provider in the message service.</span></span> 
  
<span data-ttu-id="185fb-120">A diferencia de la tabla Provider devuelta por el método [IMsgServiceAdmin:: GetProviderTable](imsgserviceadmin-getprovidertable.md) , la tabla de proveedores devuelta por **IProviderAdmin:: GetProviderTable** puede incluir filas adicionales que representan la información asociada con uno o varios de los proveedores de servicios del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="185fb-120">Unlike the provider table returned by the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method, the provider table returned by **IProviderAdmin::GetProviderTable** may include additional rows that represent information associated with one or more of the service providers in the message service.</span></span> <span data-ttu-id="185fb-121">Esta información adicional se agrega al perfil con la palabra clave "Sections" (secciones) del archivo MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="185fb-121">This extra information is added to the profile with the "Sections" keyword of the Mapisvc.inf file.</span></span> <span data-ttu-id="185fb-122">Cuando un proveedor tiene secciones de perfil adicionales, almacena las estructuras **MAPIUID** para estas secciones en la propiedad **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="185fb-122">When a provider has extra profile sections, it stores the **MAPIUID** structures for these sections in the **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)) property.</span></span> <span data-ttu-id="185fb-123">**PR_SERVICE_EXTRA_UIDS** se guarda en la sección Perfil del servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="185fb-123">**PR_SERVICE_EXTRA_UIDS** is saved in the message service profile section.</span></span> 
  
<span data-ttu-id="185fb-124">Los proveedores que se han eliminado o están en uso pero están marcados para su eliminación no se incluyen en la tabla de proveedores.</span><span class="sxs-lookup"><span data-stu-id="185fb-124">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="185fb-125">Las tablas de proveedor son estáticas, lo que significa que las adiciones o eliminaciones posteriores del servicio de mensajes no se reflejan en la tabla.</span><span class="sxs-lookup"><span data-stu-id="185fb-125">Provider tables are static, meaning that subsequent additions to or deletions from the message service are not reflected in the table.</span></span> 
  
<span data-ttu-id="185fb-126">Si el servicio de mensajes no tiene proveedores, **IProviderAdmin:: GetProviderTable** devuelve una tabla con cero filas y el valor devuelto S_OK.</span><span class="sxs-lookup"><span data-stu-id="185fb-126">If the message service has no providers, **IProviderAdmin::GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="185fb-127">La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas que se devuelven desde los métodos [IMAPITable:: QueryColumns](imapitable-querycolumns.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="185fb-127">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> 
  
<span data-ttu-id="185fb-128">Esta marca también controla los tipos de propiedades en el criterio de ordenación devueltos por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="185fb-128">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
<span data-ttu-id="185fb-129">Para obtener una lista completa de las columnas de la tabla de proveedores, consulte [TABLE Provider](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="185fb-129">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="185fb-130">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="185fb-130">Notes to callers</span></span>

<span data-ttu-id="185fb-131">Para recuperar las filas de una tabla de proveedores en orden de transporte, ordene la tabla mediante la columna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="185fb-131">To retrieve the rows of a provider table in transport order, sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
  
<span data-ttu-id="185fb-132">Para recuperar sólo las filas que representan proveedores de servicios (sin incluir ninguna fila adicional), limite la recuperación a las filas que tienen un valor de PT_ERROR en su columna **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="185fb-132">To retrieve only those rows that represent service providers (without including any extra rows), limit your retrieval to the rows that have a value of PT_ERROR in their **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) column.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="185fb-133">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="185fb-133">MFCMAPI reference</span></span>

<span data-ttu-id="185fb-134">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="185fb-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="185fb-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="185fb-135">**File**</span></span>|<span data-ttu-id="185fb-136">**Función**</span><span class="sxs-lookup"><span data-stu-id="185fb-136">**Function**</span></span>|<span data-ttu-id="185fb-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="185fb-137">**Comment**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="185fb-138">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="185fb-138">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="185fb-139">CMsgServiceTableDlg:: OnDisplayItem</span><span class="sxs-lookup"><span data-stu-id="185fb-139">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="185fb-140">MFCMAPI usa el método **IProviderAdmin:: GetProviderTable** para obtener la tabla de proveedores que se representará en un cuadro de diálogo nuevo.</span><span class="sxs-lookup"><span data-stu-id="185fb-140">MFCMAPI uses the **IProviderAdmin::GetProviderTable** method to get the table of providers to render in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="185fb-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="185fb-141">See also</span></span>



[<span data-ttu-id="185fb-142">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="185fb-142">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="185fb-143">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="185fb-143">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="185fb-144">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="185fb-144">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="185fb-145">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="185fb-145">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="185fb-146">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="185fb-146">IMsgServiceAdmin::GetProviderTable</span></span>](imsgserviceadmin-getprovidertable.md)
  
[<span data-ttu-id="185fb-147">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="185fb-147">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)


[<span data-ttu-id="185fb-148">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="185fb-148">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

