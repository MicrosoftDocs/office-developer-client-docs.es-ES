---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408729"
---
# <a name="callerrelease"></a><span data-ttu-id="0010f-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="0010f-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="0010f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0010f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0010f-105">Define una función de devolución de llamada que puede liberar un objeto de datos de tabla cuando se libera una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="0010f-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0010f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0010f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0010f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0010f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0010f-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="0010f-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="0010f-109">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="0010f-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="0010f-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="0010f-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="0010f-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="0010f-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="0010f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0010f-112">Parameters</span></span>

 <span data-ttu-id="0010f-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="0010f-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="0010f-114">[entrada] Datos del autor de la llamada guardados por MAPI con la vista de tabla y pasados a la función de devolución de llamada basada en **CALLERRELEASE.**</span><span class="sxs-lookup"><span data-stu-id="0010f-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="0010f-115">Los datos proporcionan contexto sobre la vista de tabla que se está liberando.</span><span class="sxs-lookup"><span data-stu-id="0010f-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="0010f-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="0010f-116">_lpTblData_</span></span>
  
> <span data-ttu-id="0010f-117">[entrada] Puntero a la [interfaz ITableData : IUnknown](itabledataiunknown.md) para el objeto de datos de tabla subyacente a la vista de tabla que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="0010f-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="0010f-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="0010f-118">_lpVue_</span></span>
  
> <span data-ttu-id="0010f-119">[entrada] Puntero a la [interfaz IMAPITable : IUnknown](imapitableiunknown.md) para la vista de tabla que se está liberando.</span><span class="sxs-lookup"><span data-stu-id="0010f-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="0010f-120">Se trata de una interfaz para el objeto de tabla devuelto en el parámetro  _lppMAPITable_ del método [ITableData::HrGetView](itabledata-hrgetview.md) que creó el objeto para liberar.</span><span class="sxs-lookup"><span data-stu-id="0010f-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0010f-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0010f-121">Return value</span></span>

<span data-ttu-id="0010f-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0010f-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0010f-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0010f-123">Remarks</span></span>

<span data-ttu-id="0010f-124">Una aplicación cliente o un proveedor de servicios que haya rellenado un objeto de datos de tabla puede llamar a [ITableData::HrGetView](itabledata-hrgetview.md) para crear una vista ordenada de solo lectura de la tabla.</span><span class="sxs-lookup"><span data-stu-id="0010f-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="0010f-125">La llamada a **HrGetView** pasa un puntero a una función de devolución de llamada basada en **CALLERRELEASE** y también un contexto que se guardará con la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="0010f-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="0010f-126">Cuando el recuento de referencias de la vista de tabla vuelve a cero y se libera la vista, la implementación de **IMAPITable** llama a la función de devolución de llamada y pasa el contexto en el parámetro _ulCallerData._</span><span class="sxs-lookup"><span data-stu-id="0010f-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="0010f-127">Un uso común de una función de devolución de llamada basada en **CALLERRELEASE** es liberar el objeto de datos de tabla subyacente y no es necesario realizar un seguimiento de él durante el procesamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="0010f-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

