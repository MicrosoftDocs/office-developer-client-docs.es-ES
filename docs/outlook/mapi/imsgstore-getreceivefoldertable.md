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
ms.openlocfilehash: 8146b5c2b9c9fb5429a9c1d46bca687c32bcf3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817772"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="ef0f6-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="ef0f6-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="ef0f6-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ef0f6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ef0f6-105">Proporciona acceso a la tabla de la carpeta de recepción, una tabla que incluye información acerca de todas las carpetas de recepción para el almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="ef0f6-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ef0f6-106">Parameters</span></span>

 <span data-ttu-id="ef0f6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ef0f6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ef0f6-108">[entrada] Una máscara de bits de indicadores de que los controles de la tabla de access.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="ef0f6-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="ef0f6-109">The following flags can be set:</span></span>
    
<span data-ttu-id="ef0f6-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="ef0f6-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="ef0f6-111">Permite **GetReceiveFolderTable** devolver de correctamente, posiblemente antes de la tabla es completamente disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="ef0f6-112">Si la tabla no está completamente disponible, realizar una llamada de tabla subsiguiente puede producir un error.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="ef0f6-113">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="ef0f6-114">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="ef0f6-115">Si no está establecido el indicador MAPI_UNICODE., las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="ef0f6-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ef0f6-116">_lppTable_</span></span>
  
> <span data-ttu-id="ef0f6-117">[out] Un puntero a un puntero a la tabla de la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ef0f6-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef0f6-118">Return value</span></span>

<span data-ttu-id="ef0f6-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ef0f6-119">S_OK</span></span> 
  
> <span data-ttu-id="ef0f6-120">En la tabla de la carpeta de recepción se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef0f6-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ef0f6-121">Remarks</span></span>

<span data-ttu-id="ef0f6-122">El método **IMsgStore::GetReceiveFolderTable** proporciona acceso a una tabla que muestra que los valores de propiedad para todos los del almacén de mensajes reciben las carpetas.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ef0f6-123">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="ef0f6-123">Notes to implementers</span></span>

<span data-ttu-id="ef0f6-124">Para obtener una lista de columnas obligatorias en una tabla de la carpeta de recepción, vea [Recibir carpeta tablas](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ef0f6-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="ef0f6-125">Implementar su recibir tablas de carpeta para admitir las restricciones de propiedad de configuración de la propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ef0f6-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="ef0f6-126">Este permite el acceso fácil a determinado reciben las carpetas.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ef0f6-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ef0f6-127">Notes to callers</span></span>

<span data-ttu-id="ef0f6-128">Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas desde los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="ef0f6-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="ef0f6-129">Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="ef0f6-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ef0f6-130">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ef0f6-130">MFCMAPI reference</span></span>

<span data-ttu-id="ef0f6-131">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ef0f6-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ef0f6-132">**File**</span></span>|<span data-ttu-id="ef0f6-133">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="ef0f6-133">**Function**</span></span>|<span data-ttu-id="ef0f6-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ef0f6-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef0f6-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ef0f6-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="ef0f6-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="ef0f6-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="ef0f6-137">MFCMAPI usa el método **IMsgStore::GetReceiveFolderTable** para obtener la tabla de la carpeta de recepción para mostrar.</span><span class="sxs-lookup"><span data-stu-id="ef0f6-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef0f6-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef0f6-138">See also</span></span>



[<span data-ttu-id="ef0f6-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="ef0f6-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="ef0f6-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ef0f6-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ef0f6-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="ef0f6-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="ef0f6-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="ef0f6-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="ef0f6-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ef0f6-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="ef0f6-144">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ef0f6-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
