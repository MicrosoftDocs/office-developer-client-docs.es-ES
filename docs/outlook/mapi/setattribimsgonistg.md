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
ms.openlocfilehash: e8a0daa2afe2397f39b7f37a31ef718ba65a3350
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820644"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="46593-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="46593-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="46593-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46593-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46593-105">Establece o modifica los atributos de propiedades en un objeto [IMessage](imessageimapiprop.md) proporcionado por la función [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="46593-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46593-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="46593-106">Header file:</span></span>  <br/> |<span data-ttu-id="46593-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="46593-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="46593-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="46593-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="46593-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="46593-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="46593-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="46593-110">Called by:</span></span>  <br/> |<span data-ttu-id="46593-111">Proveedores de almacén de mensajes y las aplicaciones de cliente</span><span class="sxs-lookup"><span data-stu-id="46593-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="46593-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46593-112">Parameters</span></span>

 <span data-ttu-id="46593-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="46593-113">_lpObject_</span></span>
  
> <span data-ttu-id="46593-114">[entrada] Puntero al objeto para qué propiedad se establecen los atributos.</span><span class="sxs-lookup"><span data-stu-id="46593-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="46593-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="46593-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="46593-116">[entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas (propiedad) que indica las propiedades para qué propiedad se establecen los atributos.</span><span class="sxs-lookup"><span data-stu-id="46593-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="46593-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="46593-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="46593-118">[entrada] Puntero a una estructura de [SPropAttrArray](spropattrarray.md) para establecer los atributos de propiedad de la lista.</span><span class="sxs-lookup"><span data-stu-id="46593-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="46593-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="46593-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="46593-120">[out] Puntero a la estructura [SPropProblemArray](spropproblemarray.md) devuelta que contiene un conjunto de problemas de propiedad.</span><span class="sxs-lookup"><span data-stu-id="46593-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="46593-121">Esta estructura identifica los problemas encontrados si **SetAttribIMsgOnIStg** se ha podido establecer algunas propiedades, pero no todos los.</span><span class="sxs-lookup"><span data-stu-id="46593-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="46593-122">Si se pasa un puntero a NULL en el parámetro _lppPropProblems_ , no hay ninguna matriz de problema (propiedad) se devuelve incluso si no se han establecido algunas propiedades.</span><span class="sxs-lookup"><span data-stu-id="46593-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="46593-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46593-123">Return value</span></span>

<span data-ttu-id="46593-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="46593-124">S_OK</span></span> 
  
> <span data-ttu-id="46593-125">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="46593-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="46593-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="46593-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="46593-127">La llamada satisfactoria, pero una o varias propiedades no se podrían tener acceso a y se han devuelto con un tipo de propiedad de PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="46593-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46593-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46593-128">Remarks</span></span>

<span data-ttu-id="46593-129">Sólo se pueden tener acceso a atributos de la propiedad en objetos property, es decir, objetos que implementan la [IMAPIProp: IUnknown](imapipropiunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="46593-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="46593-130">Para hacer que las propiedades MAPI esté disponible en un objeto de almacenamiento estructurado OLE, se basa [OpenIMsgOnIStg](openimsgonistg.md) un [IMessage: IMAPIProp](imessageimapiprop.md) objeto en la parte superior del objeto OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="46593-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="46593-131">Pueden establecer los atributos de propiedad en dichos objetos o modifica con **SetAttribIMsgOnIStg** y recuperar con [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="46593-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="46593-132">**Nota** **GetAttribIMsgOnIStg** y **SetAttribIMsgOnIStg** no funcionan en todos los objetos **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="46593-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="46593-133">Solo son válidos para **IMessage**- en - objetos **IStorage** devueltos por **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="46593-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="46593-134">En el parámetro _lpPropAttrs_ , el número y la posición de los atributos deben coincidir con el número y la posición de las etiquetas de propiedad que se pasa en el parámetro _lpPropTags_ .</span><span class="sxs-lookup"><span data-stu-id="46593-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="46593-135">La función **SetAttribIMsgOnIStg** se usa para realizar las propiedades del mensaje de sólo lectura cuando requeridos por el esquema de **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="46593-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="46593-136">El proveedor de almacén de mensajes de ejemplo lo usa para este propósito.</span><span class="sxs-lookup"><span data-stu-id="46593-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="46593-137">Para obtener más información, vea [los mensajes](mapi-messages.md).</span><span class="sxs-lookup"><span data-stu-id="46593-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

