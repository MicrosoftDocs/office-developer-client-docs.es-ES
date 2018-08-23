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
ms.openlocfilehash: e97e1d5302d8247cb09ce7cb1b581582405300a5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568135"
---
# <a name="callerrelease"></a><span data-ttu-id="b569a-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="b569a-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="b569a-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b569a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b569a-105">Define una función de devolución de llamada que puede liberar un objeto de datos de tabla cuando se publica una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="b569a-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b569a-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b569a-106">Header file:</span></span>  <br/> |<span data-ttu-id="b569a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b569a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b569a-108">Función definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="b569a-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="b569a-109">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="b569a-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="b569a-110">Llamado por una función definida:</span><span class="sxs-lookup"><span data-stu-id="b569a-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="b569a-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="b569a-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="b569a-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b569a-112">Parameters</span></span>

 <span data-ttu-id="b569a-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="b569a-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="b569a-114">[entrada] Datos del autor de la llamada guarda por MAPI con la vista de tabla y se pasan a la **CALLERRELEASE** en función de función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b569a-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="b569a-115">Los datos proporcionan contexto acerca de la vista de tabla que se publica.</span><span class="sxs-lookup"><span data-stu-id="b569a-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="b569a-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="b569a-116">_lpTblData_</span></span>
  
> <span data-ttu-id="b569a-117">[entrada] Puntero a la [ITableData: IUnknown](itabledataiunknown.md) interfaz para el objeto de datos de tabla subyacentes de la vista de tabla que se publica.</span><span class="sxs-lookup"><span data-stu-id="b569a-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="b569a-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="b569a-118">_lpVue_</span></span>
  
> <span data-ttu-id="b569a-119">[entrada] Puntero a la [IMAPITable: IUnknown](imapitableiunknown.md) interfaz para la vista de tabla que se publica.</span><span class="sxs-lookup"><span data-stu-id="b569a-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="b569a-120">Se trata de una interfaz para el objeto table devuelto en el parámetro _lppMAPITable_ del método [ITableData::HrGetView](itabledata-hrgetview.md) que creó el objeto para liberar.</span><span class="sxs-lookup"><span data-stu-id="b569a-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b569a-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b569a-121">Return value</span></span>

<span data-ttu-id="b569a-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b569a-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b569a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b569a-123">Remarks</span></span>

<span data-ttu-id="b569a-124">Una aplicación cliente o un proveedor de servicio que se rellena un objeto de datos de tabla puede llamar a [ITableData::HrGetView](itabledata-hrgetview.md) para crear una vista de solo lectura, ordenada de la tabla.</span><span class="sxs-lookup"><span data-stu-id="b569a-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="b569a-125">La llamada a **HrGetView** pasa un puntero a una función de devolución de llamada en función de **CALLERRELEASE** y también un contexto que se guarde con la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="b569a-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="b569a-126">Cuando se devuelve el recuento de referencia de la vista de tabla en cero y se publica la vista, la implementación de **IMAPITable** llama a la función de devolución de llamada, pasando el contexto en el parámetro _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="b569a-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="b569a-127">Un uso común de una función de devolución de llamada en función de **CALLERRELEASE** es liberar el objeto de datos de tabla subyacente y no tiene que realizar un seguimiento de durante el procesamiento subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="b569a-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

