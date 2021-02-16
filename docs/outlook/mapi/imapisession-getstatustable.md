---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407140"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="3737b-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="3737b-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="3737b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3737b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3737b-105">Proporciona acceso a la tabla de estado, una tabla que contiene información sobre todos los recursos MAPI de la sesión.</span><span class="sxs-lookup"><span data-stu-id="3737b-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="3737b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3737b-106">Parameters</span></span>

 <span data-ttu-id="3737b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3737b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3737b-108">[entrada] Máscara de bits de marcas que determina el formato de las columnas que son cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3737b-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="3737b-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="3737b-109">The following flag can be set:</span></span>
    
<span data-ttu-id="3737b-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3737b-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3737b-111">Las columnas de cadena están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="3737b-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="3737b-112">Si no MAPI_UNICODE marca, las columnas de cadena están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="3737b-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="3737b-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="3737b-113">_lppTable_</span></span>
  
> <span data-ttu-id="3737b-114">[salida] Puntero a un puntero a la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="3737b-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3737b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3737b-115">Return value</span></span>

<span data-ttu-id="3737b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3737b-116">S_OK</span></span> 
  
> <span data-ttu-id="3737b-117">La tabla se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="3737b-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3737b-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3737b-118">Remarks</span></span>

<span data-ttu-id="3737b-119">El **método IMAPISession::GetStatusTable** proporciona acceso a la tabla de estado que contiene información sobre todos los recursos MAPI de la sesión.</span><span class="sxs-lookup"><span data-stu-id="3737b-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="3737b-120">Hay una fila en la tabla para obtener información sobre el subsistema MAPI, una fila para la cola MAPI, una fila para la libreta de direcciones integrada y una fila para cada proveedor de servicios en el perfil.</span><span class="sxs-lookup"><span data-stu-id="3737b-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="3737b-121">Para obtener una lista completa de las columnas obligatorias y opcionales de la tabla de estado, vea [Tablas de estado.](status-tables.md)</span><span class="sxs-lookup"><span data-stu-id="3737b-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="3737b-122">Establecer el MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas de los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable::QueryRows.](imapitable-queryrows.md)</span><span class="sxs-lookup"><span data-stu-id="3737b-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="3737b-123">Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder.](imapitable-querysortorder.md)</span><span class="sxs-lookup"><span data-stu-id="3737b-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3737b-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3737b-124">MFCMAPI reference</span></span>

<span data-ttu-id="3737b-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="3737b-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3737b-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="3737b-126">**File**</span></span>|<span data-ttu-id="3737b-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="3737b-127">**Function**</span></span>|<span data-ttu-id="3737b-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="3737b-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3737b-129">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="3737b-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="3737b-130">CMainDlg::OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="3737b-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="3737b-131">MFCMAPI usa el **método IMAPISession::GetStatusTable** para obtener la tabla de estado que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="3737b-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3737b-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3737b-132">See also</span></span>



[<span data-ttu-id="3737b-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3737b-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="3737b-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="3737b-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="3737b-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="3737b-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="3737b-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="3737b-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="3737b-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="3737b-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="3737b-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="3737b-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="3737b-139">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3737b-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="3737b-140">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="3737b-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="3737b-141">Tablas de estado</span><span class="sxs-lookup"><span data-stu-id="3737b-141">Status Tables</span></span>](status-tables.md)

