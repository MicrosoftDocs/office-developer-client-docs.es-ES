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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338767"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="f8c12-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="f8c12-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="f8c12-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8c12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8c12-105">Proporciona acceso a la tabla de estado, una tabla que contiene información sobre todos los recursos MAPI de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f8c12-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="f8c12-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="f8c12-106">Parameters</span></span>

 <span data-ttu-id="f8c12-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8c12-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f8c12-108">a Máscara de caracteres de marcas que determina el formato de las columnas que son cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f8c12-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="f8c12-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="f8c12-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f8c12-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f8c12-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f8c12-111">Las columnas de cadena están en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f8c12-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="f8c12-112">Si no se establece la marca MAPI_UNICODE, las columnas de la cadena tienen formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f8c12-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="f8c12-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f8c12-113">_lppTable_</span></span>
  
> <span data-ttu-id="f8c12-114">contempla Un puntero a un puntero a la tabla de estado.</span><span class="sxs-lookup"><span data-stu-id="f8c12-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8c12-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8c12-115">Return value</span></span>

<span data-ttu-id="f8c12-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8c12-116">S_OK</span></span> 
  
> <span data-ttu-id="f8c12-117">La tabla se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="f8c12-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8c12-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f8c12-118">Remarks</span></span>

<span data-ttu-id="f8c12-119">El método **IMAPISession:: GetStatusTable** proporciona acceso a la tabla de estado que contiene información sobre todos los recursos MAPI de la sesión.</span><span class="sxs-lookup"><span data-stu-id="f8c12-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="f8c12-120">Hay una fila en la tabla para obtener información acerca del subsistema MAPI, una fila para la cola MAPI, una fila para la libreta de direcciones integrada y una fila para cada proveedor de servicios en el perfil.</span><span class="sxs-lookup"><span data-stu-id="f8c12-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="f8c12-121">Para obtener una lista completa de las columnas necesarias y opcionales de la tabla de estado, consulte [TABLE status](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f8c12-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="f8c12-122">La configuración de la marca MAPI_UNICODE en el parámetro _ulFlags_ afecta al formato de las columnas que se devuelven desde los métodos [IMAPITable:: QueryColumns](imapitable-querycolumns.md) y [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="f8c12-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="f8c12-123">Esta marca también controla los tipos de propiedades en el criterio de ordenación devueltos por el método [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) .</span><span class="sxs-lookup"><span data-stu-id="f8c12-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8c12-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f8c12-124">MFCMAPI reference</span></span>

<span data-ttu-id="f8c12-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f8c12-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8c12-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="f8c12-126">**File**</span></span>|<span data-ttu-id="f8c12-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="f8c12-127">**Function**</span></span>|<span data-ttu-id="f8c12-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f8c12-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8c12-129">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="f8c12-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="f8c12-130">CMainDlg:: OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="f8c12-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="f8c12-131">MFCMAPI usa el método **IMAPISession:: GetStatusTable** para obtener la tabla de estado que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="f8c12-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8c12-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8c12-132">See also</span></span>



[<span data-ttu-id="f8c12-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8c12-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="f8c12-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="f8c12-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="f8c12-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="f8c12-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="f8c12-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="f8c12-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="f8c12-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="f8c12-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="f8c12-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="f8c12-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="f8c12-139">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8c12-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f8c12-140">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="f8c12-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f8c12-141">Tablas de estado</span><span class="sxs-lookup"><span data-stu-id="f8c12-141">Status Tables</span></span>](status-tables.md)

