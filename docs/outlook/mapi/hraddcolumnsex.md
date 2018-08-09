---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c79d9ebb5be1d8af6c9136514d8a2b695513f755
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817027"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="8ba67-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="8ba67-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="8ba67-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ba67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ba67-105">Agrega o mueve las columnas al principio de una tabla existente.</span><span class="sxs-lookup"><span data-stu-id="8ba67-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8ba67-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="8ba67-106">Header file:</span></span>  <br/> |<span data-ttu-id="8ba67-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8ba67-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8ba67-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="8ba67-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8ba67-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8ba67-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8ba67-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="8ba67-110">Called by:</span></span>  <br/> |<span data-ttu-id="8ba67-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="8ba67-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a><span data-ttu-id="8ba67-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ba67-112">Parameters</span></span>

 <span data-ttu-id="8ba67-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="8ba67-113">_lptbl_</span></span>
  
> <span data-ttu-id="8ba67-114">[entrada] Puntero a la tabla MAPI afectada.</span><span class="sxs-lookup"><span data-stu-id="8ba67-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="8ba67-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="8ba67-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="8ba67-116">[entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad para las propiedades que se agreguen o se mueve al principio de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8ba67-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="8ba67-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="8ba67-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="8ba67-118">[entrada] Puntero a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) , que se usará para asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="8ba67-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="8ba67-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="8ba67-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="8ba67-120">[entrada] Puntero a la función [MAPIFreeBuffer](mapifreebuffer.md) , que se usará para liberar memoria.</span><span class="sxs-lookup"><span data-stu-id="8ba67-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="8ba67-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="8ba67-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="8ba67-122">[entrada] Puntero a una función de devolución de llamada proporcionada por el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="8ba67-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="8ba67-123">Si el parámetro _lpfnFilterColumns_ se establece en NULL, no se realiza ninguna devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8ba67-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="8ba67-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="8ba67-124">_ptaga_</span></span>
  
> <span data-ttu-id="8ba67-125">[entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene la matriz de etiquetas de propiedad ya existentes en la tabla antes de que las propiedades se agregan o se mueven al principio.</span><span class="sxs-lookup"><span data-stu-id="8ba67-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="8ba67-126">**HrAddColumnsEx** pasa este puntero como parámetro a la función de devolución de llamada que apunta _lpfnFilterColumns_.</span><span class="sxs-lookup"><span data-stu-id="8ba67-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8ba67-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ba67-127">Return value</span></span>

<span data-ttu-id="8ba67-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ba67-128">S_OK</span></span> 
  
> <span data-ttu-id="8ba67-129">La llamada se ha realizado correctamente y se han movido o agregado de las columnas especificadas.</span><span class="sxs-lookup"><span data-stu-id="8ba67-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ba67-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8ba67-130">Remarks</span></span>

<span data-ttu-id="8ba67-131">Las propiedades que se pasan a **HrAddColumnsEx** con el parámetro _lpproptagColumnsNew_ se convierten en las propiedades primera expuestas en las llamadas posteriores al método [IMAPITable:: QueryRows](imapitable-queryrows.md) .</span><span class="sxs-lookup"><span data-stu-id="8ba67-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="8ba67-132">Todas las propiedades anteriormente en la tabla que no se han especificado en el parámetro _lpproptagColumnsNew_ se exponen después de todas las propiedades agregadas y que se ha movido.</span><span class="sxs-lookup"><span data-stu-id="8ba67-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="8ba67-133">Si las propiedades de la tabla están definidas, cuando se llama a **QueryRows** , se devuelven con el tipo de propiedad PT_NULL y el identificador de la propiedad PROP_ID_NULL.</span><span class="sxs-lookup"><span data-stu-id="8ba67-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8ba67-134">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="8ba67-134">Notes to callers</span></span>

<span data-ttu-id="8ba67-135">La función **HrAddColumnsEx** permite que el autor de la llamada proporcionar una función de devolución de llamada para filtrar las columnas que ya estaban en la tabla, por ejemplo, para convertir las cadenas de tipo de propiedad PT_UNICODE a PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="8ba67-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="8ba67-136">**HrAddColumnsEx** pasa un puntero a la columna existente previamente establecido como el parámetro a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8ba67-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="8ba67-137">La función de devolución de llamada puede cambiar los datos en la matriz de la etiqueta de propiedad, pero no puede agregar nuevas etiquetas.</span><span class="sxs-lookup"><span data-stu-id="8ba67-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="8ba67-138">**HrAddColumnsEx** primero llama a la función de devolución de llamada si uno se proporciona, a continuación, agrega o mueve las columnas especificadas y, por último, llama [IMAPITable::SetColumns](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="8ba67-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="8ba67-139">Los parámetros de entrada _lpAllocateBuffer_ y _lpFreeBuffer_ apuntan a las funciones [MAPIAllocateBuffer](mapiallocatebuffer.md) y [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8ba67-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="8ba67-140">Los valores de los punteros que se pasan a **HrAddColumnsEx** exactos dependen de si el autor de la llamada es una aplicación cliente o un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="8ba67-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="8ba67-141">Un cliente pasa punteros a las funciones MAPI con los nombres especificados.</span><span class="sxs-lookup"><span data-stu-id="8ba67-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="8ba67-142">Un proveedor de servicios pasa los punteros que reciben en su llamada de inicialización o recuperar llamando al método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="8ba67-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ba67-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ba67-143">See also</span></span>



[<span data-ttu-id="8ba67-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="8ba67-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

