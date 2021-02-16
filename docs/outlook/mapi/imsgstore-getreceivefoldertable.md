---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421357"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="a8d8b-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="a8d8b-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="a8d8b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8d8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8d8b-105">Proporciona acceso a la tabla de carpetas de recepción, una tabla que incluye información sobre todas las carpetas de recepción para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="a8d8b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a8d8b-106">Parameters</span></span>

 <span data-ttu-id="a8d8b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a8d8b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a8d8b-108">[entrada] Máscara de bits de marcas que controla el acceso a las tablas.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="a8d8b-109">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="a8d8b-109">The following flags can be set:</span></span>
    
<span data-ttu-id="a8d8b-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a8d8b-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a8d8b-111">Permite **que GetReceiveFolderTable** vuelva correctamente, posiblemente antes de que la tabla esté totalmente disponible para el llamador.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="a8d8b-112">Si la tabla no está totalmente disponible, realizar una llamada de tabla posterior puede generar un error.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="a8d8b-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a8d8b-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a8d8b-114">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="a8d8b-115">Si no MAPI_UNICODE marca, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a8d8b-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a8d8b-116">_lppTable_</span></span>
  
> <span data-ttu-id="a8d8b-117">[salida] Puntero a un puntero a la tabla de la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8d8b-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8d8b-118">Return value</span></span>

<span data-ttu-id="a8d8b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8d8b-119">S_OK</span></span> 
  
> <span data-ttu-id="a8d8b-120">La tabla de carpetas de recepción se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8d8b-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8d8b-121">Remarks</span></span>

<span data-ttu-id="a8d8b-122">El **método IMsgStore::GetReceiveFolderTable** proporciona acceso a una tabla que muestra la configuración de propiedades de todas las carpetas de recepción del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a8d8b-123">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="a8d8b-123">Notes to implementers</span></span>

<span data-ttu-id="a8d8b-124">Para obtener una lista de las columnas necesarias en una tabla de carpetas de recepción, vea [Tablas de carpetas de recepción.](receive-folder-tables.md)</span><span class="sxs-lookup"><span data-stu-id="a8d8b-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="a8d8b-125">Implemente las tablas de la carpeta de recepción para admitir la configuración de restricciones de propiedad en **PR_RECORD_KEY** propiedad ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a8d8b-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="a8d8b-126">Esto permite un fácil acceso a carpetas de recepción concretas.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a8d8b-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a8d8b-127">Notes to callers</span></span>

<span data-ttu-id="a8d8b-128">Establecer el MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas de los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="a8d8b-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="a8d8b-129">Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="a8d8b-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a8d8b-130">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a8d8b-130">MFCMAPI reference</span></span>

<span data-ttu-id="a8d8b-131">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a8d8b-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="a8d8b-132">**File**</span></span>|<span data-ttu-id="a8d8b-133">**Función**</span><span class="sxs-lookup"><span data-stu-id="a8d8b-133">**Function**</span></span>|<span data-ttu-id="a8d8b-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a8d8b-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a8d8b-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a8d8b-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="a8d8b-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="a8d8b-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="a8d8b-137">MFCMAPI usa el **método IMsgStore::GetReceiveFolderTable** para obtener la tabla de carpetas de recepción que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="a8d8b-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8d8b-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8d8b-138">See also</span></span>



[<span data-ttu-id="a8d8b-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a8d8b-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="a8d8b-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="a8d8b-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="a8d8b-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a8d8b-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="a8d8b-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a8d8b-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="a8d8b-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a8d8b-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="a8d8b-144">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="a8d8b-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

