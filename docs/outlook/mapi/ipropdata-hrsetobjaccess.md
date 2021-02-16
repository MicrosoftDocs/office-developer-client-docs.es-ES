---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 4e478c9e8978125a37691ee5bd97fa9f1cbce077
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425158"
---
# <a name="ipropdatahrsetobjaccess"></a><span data-ttu-id="710d3-103">IPropData::HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="710d3-103">IPropData::HrSetObjAccess</span></span>

  
  
<span data-ttu-id="710d3-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="710d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="710d3-105">Establece el nivel de acceso para el objeto.</span><span class="sxs-lookup"><span data-stu-id="710d3-105">Sets the access level for the object.</span></span>
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="710d3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="710d3-106">Parameters</span></span>

 <span data-ttu-id="710d3-107">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="710d3-107">_ulAccess_</span></span>
  
> <span data-ttu-id="710d3-p101">[entrada] Una m�scara de bits de indicadores que especifica el nivel de acceso del objeto. Puede establecer uno de los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="710d3-p101">[in] A bitmask of flags that specifies the object's access level. One of the following flags can be set:</span></span>
    
<span data-ttu-id="710d3-110">IPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="710d3-110">IPROP_READONLY</span></span> 
  
> <span data-ttu-id="710d3-111">Establece el nivel de acceso del objeto de s�lo lectura.</span><span class="sxs-lookup"><span data-stu-id="710d3-111">Sets the object's access level to read-only.</span></span> 
    
<span data-ttu-id="710d3-112">IPROP_READWRITE</span><span class="sxs-lookup"><span data-stu-id="710d3-112">IPROP_READWRITE</span></span> 
  
> <span data-ttu-id="710d3-113">Establece el nivel de acceso del objeto para lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="710d3-113">Sets the object's access level to read/write.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="710d3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="710d3-114">Return value</span></span>

<span data-ttu-id="710d3-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="710d3-115">S_OK</span></span> 
  
> <span data-ttu-id="710d3-116">Nivel de acceso del objeto se estableci� correctamente.</span><span class="sxs-lookup"><span data-stu-id="710d3-116">The object's access level was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="710d3-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="710d3-117">Remarks</span></span>

<span data-ttu-id="710d3-p102">El m�todo **IPropData::HrSetObjAccess** establece el nivel de acceso para un objeto completo, en lugar de propiedades individuales. **HrSetObjAccess** puede utilizarse para cambiar el nivel de acceso que se estableci� cuando se cre� el objeto.</span><span class="sxs-lookup"><span data-stu-id="710d3-p102">The **IPropData::HrSetObjAccess** method sets the access level for an entire object, rather than for individual properties. **HrSetObjAccess** can be used to change the access level established when the object was created.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="710d3-120">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="710d3-120">Notes to callers</span></span>

<span data-ttu-id="710d3-p103">Para establecer un nivel de acceso de una propiedad, llamar primero a **HrSetObjAccess** con el indicador IPROP_READWRITE establecido en el par�metro  _ulAccess_ para convertir el objeto modificable. A continuaci�n, llame al m�todo de [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , especifique la propiedad de destino en la matriz que apunta el par�metro  _lpPropTagArray_.</span><span class="sxs-lookup"><span data-stu-id="710d3-p103">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable. Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="710d3-123">Para crear un objeto con las propiedades de s�lo lectura para los clientes, crear un objeto de lectura y escritura, agregue las propiedades necesarias y, a continuaci�n, llame a **HrSetObjAccess** para cambiar de acceso del objeto de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="710d3-123">To create an object with properties that will be read-only to clients, create a read/write object, add the necessary properties, and then call **HrSetObjAccess** to change the object's access to read-only.</span></span> 
  
<span data-ttu-id="710d3-124">Tambi�n puede utilizar **HrSetObjAccess** para impedir que los clientes de creaci�n de nuevas propiedades.</span><span class="sxs-lookup"><span data-stu-id="710d3-124">You can also use **HrSetObjAccess** to prevent clients from creating new properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="710d3-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="710d3-125">See also</span></span>



[<span data-ttu-id="710d3-126">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="710d3-126">IPropData::HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md)
  
[<span data-ttu-id="710d3-127">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="710d3-127">IPropData::HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md)
  
[<span data-ttu-id="710d3-128">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="710d3-128">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

