---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428833"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="61897-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="61897-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="61897-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61897-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61897-105">Establece o modifica los atributos de las propiedades de un [objeto IMessage](imessageimapiprop.md) proporcionado por la [función OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="61897-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61897-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="61897-106">Header file:</span></span>  <br/> |<span data-ttu-id="61897-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="61897-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="61897-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="61897-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="61897-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="61897-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="61897-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="61897-110">Called by:</span></span>  <br/> |<span data-ttu-id="61897-111">Proveedores de aplicaciones cliente y almacén de mensajes</span><span class="sxs-lookup"><span data-stu-id="61897-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="61897-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="61897-112">Parameters</span></span>

 <span data-ttu-id="61897-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="61897-113">_lpObject_</span></span>
  
> <span data-ttu-id="61897-114">[in] Puntero al objeto para el que se establecen los atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="61897-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="61897-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="61897-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="61897-116">[in] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las propiedades para las que se establecen los atributos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="61897-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="61897-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="61897-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="61897-118">[in] Puntero a una [estructura SPropAttrArray](spropattrarray.md) que enumera los atributos de propiedad que se establecerán.</span><span class="sxs-lookup"><span data-stu-id="61897-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="61897-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="61897-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="61897-120">[salida] Puntero a la estructura [SPropProblemArray](spropproblemarray.md) devuelta que contiene un conjunto de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="61897-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="61897-121">Esta estructura identifica los problemas detectados si **SetAttribIMsgOnIStg** ha podido establecer algunas propiedades, pero no todas.</span><span class="sxs-lookup"><span data-stu-id="61897-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="61897-122">Si se pasa un puntero a NULL en el parámetro  _lppPropProblems,_ no se devuelve ninguna matriz de problemas de propiedad incluso si algunas propiedades no se han establecido.</span><span class="sxs-lookup"><span data-stu-id="61897-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="61897-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="61897-123">Return value</span></span>

<span data-ttu-id="61897-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="61897-124">S_OK</span></span> 
  
> <span data-ttu-id="61897-125">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="61897-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="61897-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="61897-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="61897-127">La llamada se ha hecho correctamente en general, pero no se pudo obtener acceso a una o más propiedades y se devolvieron con un tipo de propiedad PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="61897-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61897-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61897-128">Remarks</span></span>

<span data-ttu-id="61897-129">Solo se puede tener acceso a los atributos de propiedad en objetos de propiedad, es decir, objetos que implementan la [interfaz IMAPIProp : IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="61897-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="61897-130">Para que las propiedades MAPI estén disponibles en un objeto de almacenamiento estructurado OLE, [OpenIMsgOnIStg](openimsgonistg.md) compila un [objeto IMessage : IMAPIProp](imessageimapiprop.md) encima del objeto OLE **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="61897-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="61897-131">Los atributos de propiedad de estos objetos se pueden establecer o modificar con **SetAttribIMsgOnIStg** y recuperarse con [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="61897-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="61897-132">**Nota** **GetAttribIMsgOnIStg** y **SetAttribIMsgOnIStg** no funcionan en todos los **objetos IMessage.**</span><span class="sxs-lookup"><span data-stu-id="61897-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="61897-133">Solo son válidos para **objetos IMessage**-on- **IStorage** devueltos **por OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="61897-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="61897-134">En el _parámetro lpPropAttrs,_ el número y la posición de los atributos deben coincidir con el número y la posición de las etiquetas de propiedad pasadas en el _parámetro lpPropTags._</span><span class="sxs-lookup"><span data-stu-id="61897-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="61897-135">La **función SetAttribIMsgOnIStg** se usa para hacer que las propiedades del mensaje de solo lectura cuando lo requiera el esquema **IMessage.**</span><span class="sxs-lookup"><span data-stu-id="61897-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="61897-136">El proveedor de almacén de mensajes de ejemplo lo usa para este propósito.</span><span class="sxs-lookup"><span data-stu-id="61897-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="61897-137">Para obtener más información, vea [Mensajes](mapi-messages.md).</span><span class="sxs-lookup"><span data-stu-id="61897-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

