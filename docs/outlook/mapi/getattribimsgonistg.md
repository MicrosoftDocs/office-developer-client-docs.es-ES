---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439999"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="f9019-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="f9019-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="f9019-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9019-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9019-105">Recupera atributos de propiedades en un [objeto IMessage](imessageimapiprop.md) proporcionado por la [función OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="f9019-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9019-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f9019-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9019-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="f9019-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="f9019-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f9019-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f9019-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f9019-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f9019-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f9019-110">Called by:</span></span>  <br/> |<span data-ttu-id="f9019-111">Aplicaciones cliente y proveedores de almacenamiento de mensajes</span><span class="sxs-lookup"><span data-stu-id="f9019-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="f9019-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9019-112">Parameters</span></span>

 <span data-ttu-id="f9019-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="f9019-113">_lpObject_</span></span>
  
> <span data-ttu-id="f9019-114">[entrada] Puntero a un **objeto IMessage** obtenido de la [función OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="f9019-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="f9019-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="f9019-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="f9019-116">[entrada] Puntero a una [estructura SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas de propiedad que indica las propiedades para las que se van a recuperar los atributos.</span><span class="sxs-lookup"><span data-stu-id="f9019-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="f9019-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="f9019-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="f9019-118">[salida] Puntero a un puntero a la estructura [SPropAttrArray](spropattrarray.md) devuelta que contiene los atributos de propiedad recuperados.</span><span class="sxs-lookup"><span data-stu-id="f9019-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f9019-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9019-119">Return value</span></span>

<span data-ttu-id="f9019-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9019-120">S_OK</span></span> 
  
> <span data-ttu-id="f9019-121">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="f9019-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="f9019-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="f9019-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="f9019-123">La llamada se ha hecho correctamente en general, pero no se pudo tener acceso a una o más propiedades y se devolvieron con un tipo de propiedad de PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="f9019-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9019-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f9019-124">Remarks</span></span>

<span data-ttu-id="f9019-125">Sólo se puede tener acceso a los atributos de propiedad en objetos de propiedad, es decir, objetos que implementan la [interfaz IMAPIProp : IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="f9019-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="f9019-126">Para que las propiedades MAPI estén disponibles en un objeto de almacenamiento estructurado OLE, [OpenIMsgOnIStg](openimsgonistg.md) genera un [objeto IMessage : IMAPIProp](imessageimapiprop.md) sobre el objeto OLE **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="f9019-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="f9019-127">Los atributos de propiedad de dichos objetos se pueden establecer o modificar [con SetAttribIMsgOnIStg](setattribimsgonistg.md) y recuperarse con **GetAttribIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="f9019-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f9019-128">**GetAttribIMsgOnIStg** y **SetAttribIMsgOnIStg** no funcionan en todos los **objetos IMessage.**</span><span class="sxs-lookup"><span data-stu-id="f9019-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="f9019-129">Solo son válidos para **objetos IMessage**-on- **IStorage** devueltos **por OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="f9019-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="f9019-130">El número y las posiciones de los atributos en el parámetro _lppPropAttrArray_ corresponden al número y las posiciones de las etiquetas de propiedad en el parámetro _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="f9019-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

