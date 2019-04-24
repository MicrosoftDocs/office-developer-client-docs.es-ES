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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331846"
---
# <a name="callerrelease"></a><span data-ttu-id="02c16-103">CALLERRELEASE</span><span class="sxs-lookup"><span data-stu-id="02c16-103">CALLERRELEASE</span></span>

  
  
<span data-ttu-id="02c16-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02c16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02c16-105">Define una función de devolución de llamada que puede liberar un objeto de datos de tabla cuando se libera una vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="02c16-105">Defines a callback function that can release a table data object when a table view is being released.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02c16-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="02c16-106">Header file:</span></span>  <br/> |<span data-ttu-id="02c16-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="02c16-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="02c16-108">Función definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="02c16-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="02c16-109">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="02c16-109">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="02c16-110">Función definida llamada por:</span><span class="sxs-lookup"><span data-stu-id="02c16-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="02c16-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="02c16-111">MAPI</span></span>  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a><span data-ttu-id="02c16-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="02c16-112">Parameters</span></span>

 <span data-ttu-id="02c16-113">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="02c16-113">_ulCallerData_</span></span>
  
> <span data-ttu-id="02c16-114">a Datos del autor de la llamada guardados por MAPI con la vista de tabla y pasados a la función de devolución de llamada basada en **CALLERRELEASE** .</span><span class="sxs-lookup"><span data-stu-id="02c16-114">[in] Caller data saved by MAPI with the table view and passed to the **CALLERRELEASE** based callback function.</span></span> <span data-ttu-id="02c16-115">Los datos proporcionan contexto sobre la vista de tabla que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="02c16-115">The data provides context about the table view being released.</span></span> 
    
 <span data-ttu-id="02c16-116">_lpTblData_</span><span class="sxs-lookup"><span data-stu-id="02c16-116">_lpTblData_</span></span>
  
> <span data-ttu-id="02c16-117">a Puntero a la interfaz [ITableData: IUnknown](itabledataiunknown.md) del objeto Table Data subyacente de la vista de tabla que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="02c16-117">[in] Pointer to the [ITableData : IUnknown](itabledataiunknown.md) interface for the table data object underlying the table view being released.</span></span> 
    
 <span data-ttu-id="02c16-118">_lpVue_</span><span class="sxs-lookup"><span data-stu-id="02c16-118">_lpVue_</span></span>
  
> <span data-ttu-id="02c16-119">a Puntero a la interfaz [IMAPITable: IUnknown](imapitableiunknown.md) para la vista de tabla que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="02c16-119">[in] Pointer to the [IMAPITable : IUnknown](imapitableiunknown.md) interface for the table view being released.</span></span> <span data-ttu-id="02c16-120">Se trata de una interfaz para el objeto Table devuelto en el parámetro _lppMAPITable_ del método [ITableData:: HrGetView](itabledata-hrgetview.md) que creó el objeto que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="02c16-120">This is an interface for the table object returned in the  _lppMAPITable_ parameter of the [ITableData::HrGetView](itabledata-hrgetview.md) method that created the object to release.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="02c16-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="02c16-121">Return value</span></span>

<span data-ttu-id="02c16-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="02c16-122">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="02c16-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="02c16-123">Remarks</span></span>

<span data-ttu-id="02c16-124">Una aplicación cliente o un proveedor de servicios que ha rellenado un objeto Table Data puede llamar a [ITableData:: HrGetView](itabledata-hrgetview.md) para crear una vista ordenada de solo lectura de la tabla.</span><span class="sxs-lookup"><span data-stu-id="02c16-124">A client application or service provider that has populated a table data object can call [ITableData::HrGetView](itabledata-hrgetview.md) to create a read-only, sorted view of the table.</span></span> <span data-ttu-id="02c16-125">La llamada a **HrGetView** pasa un puntero a una función de devolución de llamada basada en **CALLERRELEASE** y también un contexto que se va a guardar con la vista de tabla.</span><span class="sxs-lookup"><span data-stu-id="02c16-125">The call to **HrGetView** passes a pointer to a **CALLERRELEASE** based callback function and also a context to be saved with the table view.</span></span> <span data-ttu-id="02c16-126">Cuando el recuento de referencias de la vista de tabla vuelve a cero y se suelta la vista, la implementación de **IMAPITable** llama a la función de devolución de llamada, pasando el contexto en el parámetro _ulCallerData_ .</span><span class="sxs-lookup"><span data-stu-id="02c16-126">When the reference count of the table view returns to zero and the view is being released, the **IMAPITable** implementation calls the callback function, passing the context in the  _ulCallerData_ parameter.</span></span> 
  
<span data-ttu-id="02c16-127">Un uso común de una función de devolución de llamada basada en **CALLERRELEASE** es liberar el objeto de datos de tabla subyacente y no tener que realizar un seguimiento durante el procesamiento posterior.</span><span class="sxs-lookup"><span data-stu-id="02c16-127">A common use of a **CALLERRELEASE** based callback function is to release the underlying table data object and not have to keep track of it during subsequent processing.</span></span> 
  

