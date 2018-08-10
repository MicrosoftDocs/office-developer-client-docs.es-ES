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
ms.openlocfilehash: ba540b0fd3371b3e12be9eeeb102a9bd9d7e8d22
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817430"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="e267b-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="e267b-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="e267b-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e267b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e267b-105">Proporciona acceso a la tabla de almacenamiento de mensaje que contiene información acerca de todos los almacenes de mensaje en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="e267b-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="e267b-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="e267b-106">Parameters</span></span>

 <span data-ttu-id="e267b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e267b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e267b-108">[entrada] Una máscara de bits de indicadores que determina el formato para las columnas que son cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e267b-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="e267b-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="e267b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e267b-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e267b-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e267b-111">Las columnas de cadena se encuentran en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e267b-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="e267b-112">Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e267b-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="e267b-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="e267b-113">_lppTable_</span></span>
  
> <span data-ttu-id="e267b-114">[out] Un puntero a un puntero a la tabla de almacén de mensajes.</span><span class="sxs-lookup"><span data-stu-id="e267b-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e267b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e267b-115">Return value</span></span>

<span data-ttu-id="e267b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e267b-116">S_OK</span></span> 
  
> <span data-ttu-id="e267b-117">En la tabla se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="e267b-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="e267b-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="e267b-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="e267b-119">Se ha establecido el indicador MAPI_UNICODE y la sesión no es compatible con Unicode.</span><span class="sxs-lookup"><span data-stu-id="e267b-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e267b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e267b-120">Remarks</span></span>

<span data-ttu-id="e267b-121">El método **IMAPISession::GetMsgStoresTable** recupera un puntero a la tabla de almacenamiento de mensajes, una tabla que mantienen MAPI que contiene información acerca de cada almacén de abrir el mensaje en el perfil.</span><span class="sxs-lookup"><span data-stu-id="e267b-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="e267b-122">Para obtener una lista completa de columnas obligatorias y opcionales en el mensaje almacén tabla, consulte [Tablas de almacén de mensajes](message-store-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e267b-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e267b-123">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="e267b-123">Notes to callers</span></span>

<span data-ttu-id="e267b-124">Debido a que MAPI actualiza la tabla de almacenamiento de mensaje durante la sesión cuando se producen cambios, llame al método **Advise** de la tabla de almacenamiento de mensajes para registrarse para recibir notificaciones de estos cambios.</span><span class="sxs-lookup"><span data-stu-id="e267b-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="e267b-125">Posibles cambios incluyen la adición de nuevos almacenes de mensaje, almacena la eliminación de los existentes y los cambios en el almacén predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e267b-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="e267b-126">Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas desde los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="e267b-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="e267b-127">Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="e267b-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e267b-128">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e267b-128">MFCMAPI reference</span></span>

<span data-ttu-id="e267b-129">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e267b-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e267b-130">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e267b-130">**File**</span></span>|<span data-ttu-id="e267b-131">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="e267b-131">**Function**</span></span>|<span data-ttu-id="e267b-132">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e267b-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e267b-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e267b-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="e267b-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="e267b-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="e267b-135">MFCMAPI utiliza el método **IMAPISession::GetMsgStoresTable** para obtener la tabla de almacenamiento de mensajes para que se puede representar en el cuadro de diálogo principal de MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="e267b-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e267b-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="e267b-136">See also</span></span>



[<span data-ttu-id="e267b-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="e267b-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="e267b-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e267b-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="e267b-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="e267b-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="e267b-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="e267b-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="e267b-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="e267b-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="e267b-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="e267b-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="e267b-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e267b-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="e267b-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e267b-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="e267b-145">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="e267b-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e267b-146">Tablas de almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="e267b-146">Message Store Tables</span></span>](message-store-tables.md)

