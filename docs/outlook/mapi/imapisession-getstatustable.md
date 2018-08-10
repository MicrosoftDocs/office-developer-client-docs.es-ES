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
ms.openlocfilehash: 7de404f421a405d80dd7f98beba5168969222fc9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817445"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="a51bb-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="a51bb-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="a51bb-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a51bb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a51bb-105">Proporciona acceso a la tabla de estado, una tabla que contiene información acerca de todos los recursos MAPI en la sesión.</span><span class="sxs-lookup"><span data-stu-id="a51bb-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="a51bb-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="a51bb-106">Parameters</span></span>

 <span data-ttu-id="a51bb-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a51bb-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a51bb-108">[entrada] Una máscara de bits de indicadores que determina el formato para las columnas que son cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a51bb-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="a51bb-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="a51bb-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a51bb-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="a51bb-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a51bb-111">Las columnas de cadena se encuentran en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a51bb-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="a51bb-112">Si no está establecido el indicador MAPI_UNICODE., las columnas de cadena están en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a51bb-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="a51bb-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="a51bb-113">_lppTable_</span></span>
  
> <span data-ttu-id="a51bb-114">[out] Un puntero a un puntero a la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="a51bb-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a51bb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a51bb-115">Return value</span></span>

<span data-ttu-id="a51bb-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="a51bb-116">S_OK</span></span> 
  
> <span data-ttu-id="a51bb-117">En la tabla se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="a51bb-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a51bb-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a51bb-118">Remarks</span></span>

<span data-ttu-id="a51bb-119">El método **IMAPISession::GetStatusTable** proporciona acceso a la tabla de estado que contiene información acerca de todos los recursos MAPI en la sesión.</span><span class="sxs-lookup"><span data-stu-id="a51bb-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="a51bb-120">No hay una fila en la tabla para obtener información sobre el subsistema MAPI, una fila de la cola MAPI, una fila de la libreta de direcciones integrada y una fila por cada proveedor de servicios en el perfil.</span><span class="sxs-lookup"><span data-stu-id="a51bb-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="a51bb-121">Para obtener una lista completa de las columnas obligatorias y opcionales en la tabla de estado, vea [Las tablas de estado](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="a51bb-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="a51bb-122">Establecer el indicador MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas devueltas desde los métodos [IMAPITable::QueryColumns](imapitable-querycolumns.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="a51bb-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="a51bb-123">Esta marca también controla los tipos de propiedad en el criterio de ordenación devuelto por el método [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="a51bb-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a51bb-124">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a51bb-124">MFCMAPI reference</span></span>

<span data-ttu-id="a51bb-125">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="a51bb-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a51bb-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="a51bb-126">**File**</span></span>|<span data-ttu-id="a51bb-127">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="a51bb-127">**Function**</span></span>|<span data-ttu-id="a51bb-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="a51bb-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a51bb-129">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a51bb-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="a51bb-130">CMainDlg::OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="a51bb-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="a51bb-131">MFCMAPI utiliza el método **IMAPISession::GetStatusTable** para obtener la tabla de estado que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="a51bb-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a51bb-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a51bb-132">See also</span></span>



[<span data-ttu-id="a51bb-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a51bb-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="a51bb-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="a51bb-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="a51bb-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="a51bb-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="a51bb-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="a51bb-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="a51bb-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a51bb-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="a51bb-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="a51bb-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="a51bb-139">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a51bb-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="a51bb-140">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="a51bb-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a51bb-141">Tablas de estado</span><span class="sxs-lookup"><span data-stu-id="a51bb-141">Status Tables</span></span>](status-tables.md)
