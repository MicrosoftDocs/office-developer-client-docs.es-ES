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
ms.openlocfilehash: 9e17e8ef7df33ffa248eec4195c00c77d0c49f94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587771"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="24834-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="24834-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="24834-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24834-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24834-105">Recupera los atributos de propiedades en un objeto [IMessage](imessageimapiprop.md) proporcionado por la función [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="24834-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24834-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="24834-106">Header file:</span></span>  <br/> |<span data-ttu-id="24834-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="24834-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="24834-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="24834-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="24834-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="24834-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="24834-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="24834-110">Called by:</span></span>  <br/> |<span data-ttu-id="24834-111">Proveedores de almacén de mensajes y las aplicaciones de cliente</span><span class="sxs-lookup"><span data-stu-id="24834-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="24834-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24834-112">Parameters</span></span>

 <span data-ttu-id="24834-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="24834-113">_lpObject_</span></span>
  
> <span data-ttu-id="24834-114">[entrada] Puntero a un objeto **IMessage** obtenido de la función [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="24834-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="24834-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="24834-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="24834-116">[entrada] Puntero a una estructura de [elemento SPropTagArray](sproptagarray.md) que contiene una matriz de etiquetas (propiedad) que indica las propiedades para que los atributos se van a recuperar.</span><span class="sxs-lookup"><span data-stu-id="24834-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="24834-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="24834-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="24834-118">[out] Puntero a un puntero a la estructura [SPropAttrArray](spropattrarray.md) devuelta que contiene los atributos de la propiedad recuperada.</span><span class="sxs-lookup"><span data-stu-id="24834-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="24834-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24834-119">Return value</span></span>

<span data-ttu-id="24834-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="24834-120">S_OK</span></span> 
  
> <span data-ttu-id="24834-121">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="24834-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="24834-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="24834-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="24834-123">La llamada satisfactoria, pero una o varias propiedades no se podrían tener acceso a y se han devuelto con un tipo de propiedad de PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="24834-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24834-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24834-124">Remarks</span></span>

<span data-ttu-id="24834-125">Sólo se pueden tener acceso a atributos de la propiedad en objetos property, es decir, objetos que implementan la [IMAPIProp: IUnknown](imapipropiunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="24834-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="24834-126">Para hacer que las propiedades MAPI esté disponible en un objeto de almacenamiento estructurado OLE, se basa [OpenIMsgOnIStg](openimsgonistg.md) un [IMessage: IMAPIProp](imessageimapiprop.md) objeto en la parte superior del objeto OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="24834-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="24834-127">Pueden establecer los atributos de propiedad en dichos objetos o modifica con [SetAttribIMsgOnIStg](setattribimsgonistg.md) y recuperar con **GetAttribIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="24834-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="24834-128">**GetAttribIMsgOnIStg** y **SetAttribIMsgOnIStg** no funcionan en todos los objetos **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="24834-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="24834-129">Solo son válidos para **IMessage**- en - objetos **IStorage** devueltos por **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="24834-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="24834-130">El número y las posiciones de los atributos en el parámetro _lppPropAttrArray_ se corresponden con el número y las posiciones de las etiquetas de propiedad en el parámetro _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="24834-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

