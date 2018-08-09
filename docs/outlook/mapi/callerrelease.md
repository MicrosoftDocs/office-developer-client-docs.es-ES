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
ms.openlocfilehash: 69ee06ef8c8f5499dec41232d3dc7b374b15a744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816501"
---
# <a name="callerrelease"></a><span data-ttu-id="4d6e2-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="4d6e2-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="4d6e2-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4d6e2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4d6e2-105">Define una función de devolución de llamada que puede liberar un objeto de datos de tabla cuando se publica una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="4d6e2-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4d6e2-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4d6e2-106">Header file:</span></span>  <br/> |<span data-ttu-id="4d6e2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4d6e2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4d6e2-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="4d6e2-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="4d6e2-109">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="4d6e2-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="4d6e2-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="4d6e2-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="4d6e2-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="4d6e2-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="4d6e2-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4d6e2-112">Parameters</span></span>

 <span data-ttu-id="4d6e2-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="4d6e2-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="4d6e2-114">[entrada] Datos del autor de la llamada guarda por MAPI con la vista de tabla y se pasan a la **CALLERRELEASE** en función de función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="4d6e2-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="4d6e2-115">Los datos proporcionan contexto acerca de la vista de tabla que se publica.</span><span class="sxs-lookup"><span data-stu-id="4d6e2-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="4d6e2-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="4d6e2-116">_lpTblData_</span></span>
  
> <span data-ttu-id="4d6e2-117">[entrada] Puntero a la [ITableData: IUnknown](itabledataiunknown.md) interfaz para el objeto de datos de tabla subyacentes de la vista de tabla que se publica.</span><span class="sxs-lookup"><span data-stu-id="4d6e2-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="4d6e2-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="4d6e2-118">_lpVue_</span></span>
  
> <span data-ttu-id="4d6e2-119">[entrada] Puntero a la [IMAPITable: IUnknown](imapitableiunknown.md) interfaz para la vista de tabla que se publica.</span><span class="sxs-lookup"><span data-stu-id="4d6e2-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="4d6e2-120">Se trata de una interfaz para el objeto table devuelto en el parámetro _lppMAPITable_ del método [ITableData::HrGetView](itabledata-hrgetview.md) que creó el objeto para liberar.</span><span class="sxs-lookup"><span data-stu-id="4d6e2-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4d6e2-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4d6e2-121">Return value</span></span>

<span data-ttu-id="4d6e2-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4d6e2-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4d6e2-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d6e2-123">Remarks</span></span>

<span data-ttu-id="4d6e2-124">Una aplicación cliente o un proveedor de servicio que se rellena un objeto de datos de tabla puede llamar a [ITableData::HrGetView](itabledata-hrgetview.md) para crear una vista de solo lectura, ordenada de la tabla.</span><span class="sxs-lookup"><span data-stu-id="4d6e2-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="4d6e2-125">La llamada a **HrGetView** pasa un puntero a una función de devolución de llamada en función de **CALLERRELEASE** y también un contexto que se guarde con la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="4d6e2-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="4d6e2-126">Cuando se devuelve el recuento de referencia de la vista de tabla en cero y se publica la vista, la implementación de **IMAPITable** llama a la función de devolución de llamada, pasando el contexto en el parámetro _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="4d6e2-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="4d6e2-127">Un uso común de una función de devolución de llamada en función de **CALLERRELEASE** es liberar el objeto de datos de tabla subyacente y no tiene que realizar un seguimiento de durante el procesamiento subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="4d6e2-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

