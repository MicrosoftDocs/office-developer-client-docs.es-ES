---
title: IMsgServiceAdminGetProviderTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetProviderTable
api_type:
- COM
ms.assetid: 7180bff2-91ad-4e11-923e-2a9acefa3215
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1185a35df471fc3f85cbf50fd8ad3baa3927e72b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317384"
---
# <a name="imsgserviceadmingetprovidertable"></a><span data-ttu-id="6dd6a-103">IMsgServiceAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="6dd6a-103">IMsgServiceAdmin::GetProviderTable</span></span>

  
  
<span data-ttu-id="6dd6a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6dd6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6dd6a-105">Proporciona acceso a la tabla de proveedores, una lista de los proveedores de servicios del perfil.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-105">Provides access to the provider table, a listing of the service providers in the profile.</span></span>
  
```cpp
HRESULT GetProviderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6dd6a-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6dd6a-106">Parameters</span></span>

 <span data-ttu-id="6dd6a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6dd6a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6dd6a-108">a Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="6dd6a-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6dd6a-109">_lppTable_</span></span>
  
> <span data-ttu-id="6dd6a-110">contempla Un puntero a un puntero a la tabla del proveedor.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-110">[out] A pointer to a pointer to the provider table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6dd6a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6dd6a-111">Return value</span></span>

<span data-ttu-id="6dd6a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="6dd6a-112">S_OK</span></span> 
  
> <span data-ttu-id="6dd6a-113">La tabla de proveedores se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-113">The provider table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6dd6a-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6dd6a-114">Remarks</span></span>

<span data-ttu-id="6dd6a-115">El método **IMsgServiceAdmin:: GetProviderTable** proporciona acceso a la tabla de proveedores de MAPI, una tabla que enumera todos los proveedores de libreta de direcciones, de almacén de mensajes y de transporte instalados actualmente en el perfil.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-115">The **IMsgServiceAdmin::GetProviderTable** method provides access to the MAPI provider table, a table that lists all the address book, message store, and transport providers currently installed in the profile.</span></span> 
  
<span data-ttu-id="6dd6a-116">A diferencia de la tabla Provider devuelta a través del método [IProviderAdmin:: GetProviderTable](iprovideradmin-getprovidertable.md) , la tabla de proveedores devuelta por **IMsgServiceAdmin:: GetProviderTable** no puede incluir más filas que representen la información asociada con uno o más proveedores de servicios en el perfil.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-116">Unlike the provider table returned through the [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) method, the provider table returned through **IMsgServiceAdmin::GetProviderTable** cannot include additional rows that represent information associated with one or more service providers in the profile.</span></span> 
  
<span data-ttu-id="6dd6a-117">Los proveedores que se han eliminado o están en uso pero están marcados para su eliminación no se incluyen en la tabla de proveedores.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-117">Providers that have been deleted, or are in use but have been marked for deletion, are not included in the provider table.</span></span> <span data-ttu-id="6dd6a-118">Las tablas de proveedor son estáticas, lo que significa que las adiciones o eliminaciones posteriores del perfil no se reflejan en la tabla.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-118">Provider tables are static, meaning that subsequent additions to or deletions from the profile are not reflected in the table.</span></span> 
  
<span data-ttu-id="6dd6a-119">Si el perfil no tiene proveedores, **GetProviderTable** devuelve una tabla con cero filas y el valor devuelto S_OK.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-119">If the profile has no providers, **GetProviderTable** returns a table with zero rows and the S_OK return value.</span></span> 
  
<span data-ttu-id="6dd6a-120">Para obtener una lista completa de las columnas de la tabla de proveedores, consulte [TABLE Provider](provider-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6dd6a-120">For a complete list of the columns in the provider table, see [Provider Table](provider-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6dd6a-121">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="6dd6a-121">Notes to callers</span></span>

<span data-ttu-id="6dd6a-122">Para recuperar las filas de una tabla de proveedores en el orden de transporte, use el procedimiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="6dd6a-122">To retrieve the rows of a provider table in transport order, use the following procedure:</span></span>
  
1. <span data-ttu-id="6dd6a-123">Llame al método [IMAPITable:: Restrict](imapitable-restrict.md) para imponer una restricción de propiedad que coincida con la propiedad **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) con MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-123">Call the [IMAPITable::Restrict](imapitable-restrict.md) method to impose a property restriction that matches the **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) property with MAPI_TRANSPORT_PROVIDER.</span></span>
    
2. <span data-ttu-id="6dd6a-124">Llame al método [IMAPITable:: SortTable](imapitable-sorttable.md) para ordenar la tabla por la columna **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6dd6a-124">Call the [IMAPITable::SortTable](imapitable-sorttable.md) method to sort the table by the **PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md)) column.</span></span> 
    
3. <span data-ttu-id="6dd6a-125">Llame al método [IMAPITable:: QueryRows](imapitable-queryrows.md) para obtener las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-125">Call the [IMAPITable::QueryRows](imapitable-queryrows.md) method to get the rows of the table.</span></span> 
    
<span data-ttu-id="6dd6a-126">Una alternativa a estas llamadas es realizar una única llamada a la función [HrQueryAllRows](hrqueryallrows.md) con todas las estructuras de datos adecuadas que se pasan.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-126">An alternative to these calls is to make a single call to the [HrQueryAllRows](hrqueryallrows.md) function with all of the appropriate data structures passed in.</span></span> 
  
<span data-ttu-id="6dd6a-127">Si recupera las columnas **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) en cada una de las filas, puede usar esta matriz de estructuras **MAPIUID** para establecer el orden de transporte en una llamada a [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span><span class="sxs-lookup"><span data-stu-id="6dd6a-127">If you retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) columns in each of the rows, you can use this array of **MAPIUID** structures to set the transport order in a call to [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).</span></span>
  
<span data-ttu-id="6dd6a-128">La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ hace lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6dd6a-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter does the following:</span></span> 
  
- <span data-ttu-id="6dd6a-129">Establece el tipo de cadena en Unicode para los datos devueltos por el método [IMAPITable:: QueryColumns](imapitable-querycolumns.md) para las columnas activas iniciales de la tabla del proveedor.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-129">Sets the string type to Unicode for data returned for the initial active columns of the provider table by the [IMAPITable::QueryColumns](imapitable-querycolumns.md) method.</span></span> <span data-ttu-id="6dd6a-130">Las columnas activas iniciales de una tabla de proveedor son las columnas que el método **QueryColumns** devuelve antes de que el proveedor que contiene la tabla llame al método [IMAPITable:: SetColumns](imapitable-setcolumns.md) .</span><span class="sxs-lookup"><span data-stu-id="6dd6a-130">The initial active columns for a provider table are those columns the **QueryColumns** method returns before the provider that contains the table calls the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
    
- <span data-ttu-id="6dd6a-131">Establece el tipo de cadena en Unicode para los datos devueltos por las filas activas iniciales de la tabla de proveedores mediante **QueryRows**.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-131">Sets the string type to Unicode for data returned for the initial active rows of the provider table by **QueryRows**.</span></span> <span data-ttu-id="6dd6a-132">Las filas activas iniciales de una tabla Provider son las filas **QueryRows** devuelven antes de que el proveedor que contiene la tabla llame a **SetColumns**.</span><span class="sxs-lookup"><span data-stu-id="6dd6a-132">The initial active rows for a provider table are those rows **QueryRows** returns before the provider that contains the table calls **SetColumns**.</span></span> 
    
- <span data-ttu-id="6dd6a-133">Controla los tipos de propiedades del criterio de ordenación devuelto por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) antes de que el cliente que contiene la tabla de proveedores llame al método [IMAPITable:: SortTable](imapitable-sorttable.md) .</span><span class="sxs-lookup"><span data-stu-id="6dd6a-133">Controls the property types of the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method before the client that contains the provider table calls the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6dd6a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="6dd6a-134">See also</span></span>



[<span data-ttu-id="6dd6a-135">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="6dd6a-135">IMsgServiceAdmin::GetMsgServiceTable</span></span>](imsgserviceadmin-getmsgservicetable.md)
  
[<span data-ttu-id="6dd6a-136">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="6dd6a-136">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>](imsgserviceadmin-msgservicetransportorder.md)
  
[<span data-ttu-id="6dd6a-137">IProviderAdmin::GetProviderTable</span><span class="sxs-lookup"><span data-stu-id="6dd6a-137">IProviderAdmin::GetProviderTable</span></span>](iprovideradmin-getprovidertable.md)
  
[<span data-ttu-id="6dd6a-138">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6dd6a-138">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

