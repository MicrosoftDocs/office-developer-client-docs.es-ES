---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428140"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="35548-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="35548-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="35548-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="35548-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="35548-105">Proporciona acceso a la tabla del almacén de mensajes que contiene información sobre todos los almacenes de mensajes en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="35548-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="35548-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35548-106">Parameters</span></span>

 <span data-ttu-id="35548-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="35548-107">_ulFlags_</span></span>
  
> <span data-ttu-id="35548-108">[entrada] Máscara de bits de marcas que determina el formato de las columnas que son cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="35548-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="35548-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="35548-109">The following flag can be set:</span></span>
    
<span data-ttu-id="35548-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="35548-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="35548-111">Las columnas de cadena están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="35548-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="35548-112">Si no MAPI_UNICODE marca, las columnas de cadena están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="35548-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="35548-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="35548-113">_lppTable_</span></span>
  
> <span data-ttu-id="35548-114">[salida] Puntero a un puntero a la tabla del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="35548-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35548-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35548-115">Return value</span></span>

<span data-ttu-id="35548-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="35548-116">S_OK</span></span> 
  
> <span data-ttu-id="35548-117">La tabla se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="35548-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="35548-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="35548-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="35548-119">Se MAPI_UNICODE marca y la sesión no admite Unicode.</span><span class="sxs-lookup"><span data-stu-id="35548-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="35548-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="35548-120">Remarks</span></span>

<span data-ttu-id="35548-121">El **método IMAPISession::GetMsgStoresTable** recupera un puntero a la tabla del almacén de mensajes, una tabla mantenida por MAPI que contiene información sobre cada almacén de mensajes abierto en el perfil.</span><span class="sxs-lookup"><span data-stu-id="35548-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="35548-122">Para obtener una lista completa de las columnas obligatorias y opcionales de la tabla del almacén de mensajes, vea [Tablas del almacén de mensajes.](message-store-tables.md)</span><span class="sxs-lookup"><span data-stu-id="35548-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="35548-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="35548-123">Notes to callers</span></span>

<span data-ttu-id="35548-124">Dado que MAPI actualiza la tabla del almacén de mensajes durante la sesión siempre que se produzcan cambios, llame al método **Advise** de la tabla del almacén de mensajes para registrarse para recibir una notificación de estos cambios.</span><span class="sxs-lookup"><span data-stu-id="35548-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="35548-125">Los cambios posibles incluyen la adición de nuevos almacenes de mensajes, la eliminación de almacenes existentes y los cambios en el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="35548-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="35548-126">Establecer el MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas de los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="35548-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="35548-127">Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el [método IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="35548-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="35548-128">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="35548-128">MFCMAPI reference</span></span>

<span data-ttu-id="35548-129">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="35548-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="35548-130">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="35548-130">**File**</span></span>|<span data-ttu-id="35548-131">**Función**</span><span class="sxs-lookup"><span data-stu-id="35548-131">**Function**</span></span>|<span data-ttu-id="35548-132">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="35548-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="35548-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="35548-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="35548-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="35548-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="35548-135">MFCMAPI usa el método **IMAPISession::GetMsgStoresTable** para obtener la tabla del almacén de mensajes de modo que se pueda representar en el cuadro de diálogo principal de MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="35548-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="35548-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="35548-136">See also</span></span>



[<span data-ttu-id="35548-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="35548-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="35548-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="35548-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="35548-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="35548-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="35548-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="35548-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="35548-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="35548-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="35548-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="35548-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="35548-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="35548-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="35548-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="35548-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="35548-145">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="35548-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="35548-146">Tablas del almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="35548-146">Message Store Tables</span></span>](message-store-tables.md)

