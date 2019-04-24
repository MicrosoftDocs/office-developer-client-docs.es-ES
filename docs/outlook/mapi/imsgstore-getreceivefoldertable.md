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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317356"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="a65d0-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="a65d0-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="a65d0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a65d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a65d0-105">Proporciona acceso a la tabla de la carpeta de recepción, una tabla que incluye información acerca de todas las carpetas de recepción del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a65d0-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="a65d0-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a65d0-106">Parameters</span></span>

 <span data-ttu-id="a65d0-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a65d0-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a65d0-108">a Máscara de máscara de marcadores que controla el acceso a la tabla.</span><span class="sxs-lookup"><span data-stu-id="a65d0-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="a65d0-109">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="a65d0-109">The following flags can be set:</span></span>
    
<span data-ttu-id="a65d0-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="a65d0-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="a65d0-111">Permite que **GetReceiveFolderTable** vuelva correctamente, posiblemente antes de que la tabla esté completamente disponible para el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="a65d0-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="a65d0-112">Si la tabla no está completamente disponible, puede producirse un error si se realiza una llamada posterior a la tabla.</span><span class="sxs-lookup"><span data-stu-id="a65d0-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="a65d0-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a65d0-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a65d0-114">Las cadenas devueltas están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a65d0-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="a65d0-115">Si no se establece la marca MAPI_UNICODE, las cadenas están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a65d0-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a65d0-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a65d0-116">_lppTable_</span></span>
  
> <span data-ttu-id="a65d0-117">contempla Un puntero a un puntero a la tabla de la carpeta de recepción.</span><span class="sxs-lookup"><span data-stu-id="a65d0-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a65d0-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a65d0-118">Return value</span></span>

<span data-ttu-id="a65d0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a65d0-119">S_OK</span></span> 
  
> <span data-ttu-id="a65d0-120">La tabla de recepción de la carpeta se ha devuelto correctamente.</span><span class="sxs-lookup"><span data-stu-id="a65d0-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a65d0-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a65d0-121">Remarks</span></span>

<span data-ttu-id="a65d0-122">El método **IMsgStore:: GetReceiveFolderTable** proporciona acceso a una tabla que muestra la configuración de las propiedades de todas las carpetas de recepción del almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="a65d0-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a65d0-123">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="a65d0-123">Notes to implementers</span></span>

<span data-ttu-id="a65d0-124">Para obtener una lista de las columnas necesarias en una tabla de carpetas de recepción, consulte [Receive Folder tables](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a65d0-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="a65d0-125">Implemente las tablas de la carpeta de recepción para admitir la configuración de restricciones de propiedad en la propiedad **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a65d0-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="a65d0-126">Esto permite un acceso sencillo a determinadas carpetas de recepción.</span><span class="sxs-lookup"><span data-stu-id="a65d0-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="a65d0-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a65d0-127">Notes to callers</span></span>

<span data-ttu-id="a65d0-128">La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas que se devuelven desde los métodos [IMAPITable:: QueryColumns](imapitable-querycolumns.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="a65d0-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="a65d0-129">Esta marca también controla los tipos de propiedades en el criterio de ordenación devueltos por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="a65d0-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a65d0-130">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a65d0-130">MFCMAPI reference</span></span>

<span data-ttu-id="a65d0-131">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a65d0-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a65d0-132">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="a65d0-132">**File**</span></span>|<span data-ttu-id="a65d0-133">**Función**</span><span class="sxs-lookup"><span data-stu-id="a65d0-133">**Function**</span></span>|<span data-ttu-id="a65d0-134">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a65d0-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a65d0-135">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="a65d0-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="a65d0-136">CMsgStoreDlg:: OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="a65d0-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="a65d0-137">MFCMAPI usa el método **IMsgStore:: GetReceiveFolderTable** para obtener la tabla de la carpeta de recepción que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="a65d0-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a65d0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="a65d0-138">See also</span></span>



[<span data-ttu-id="a65d0-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a65d0-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="a65d0-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="a65d0-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="a65d0-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a65d0-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="a65d0-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a65d0-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="a65d0-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a65d0-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="a65d0-144">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="a65d0-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

