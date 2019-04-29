---
title: IMAPIFormFactoryCreateClassFactory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.CreateClassFactory
api_type:
- COM
ms.assetid: dceb21b1-be5e-418d-b0c9-db39195fc82e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6e616a76d9665b602184e88566384506fcce5697
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416079"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="20165-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="20165-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="20165-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20165-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20165-105">Devuelve un objeto de generador de clases para el formulario.</span><span class="sxs-lookup"><span data-stu-id="20165-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="20165-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="20165-106">Parameters</span></span>

 <span data-ttu-id="20165-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="20165-107">_clsidForm_</span></span>
  
> <span data-ttu-id="20165-108">a Identificador de clase para el formulario que el generador de clases va a crear.</span><span class="sxs-lookup"><span data-stu-id="20165-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="20165-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="20165-109">_ulFlags_</span></span>
  
> <span data-ttu-id="20165-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="20165-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="20165-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="20165-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="20165-112">contempla Un puntero al objeto generador de clases.</span><span class="sxs-lookup"><span data-stu-id="20165-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="20165-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20165-113">Return value</span></span>

<span data-ttu-id="20165-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="20165-114">S_OK</span></span> 
  
> <span data-ttu-id="20165-115">Se devolvió el objeto de generador de clases.</span><span class="sxs-lookup"><span data-stu-id="20165-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="20165-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20165-116">Remarks</span></span>

<span data-ttu-id="20165-117">Los visores de formularios llaman al método **IMAPIFormFactory:: CreateClassFactory** para obtener un generador de clases para un formulario específico.</span><span class="sxs-lookup"><span data-stu-id="20165-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="20165-118">El generador de clases se usa para crear instancias de un formulario que controla mensajes de una clase específica y para controlar el acceso a estas instancias.</span><span class="sxs-lookup"><span data-stu-id="20165-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="20165-119">Los visores de formulario llaman al método **CreateClassFactory** para obtener un objeto de generador de clases para servidores de formularios que implementen varias clases de mensajes.</span><span class="sxs-lookup"><span data-stu-id="20165-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="20165-120">Este método recibe un identificador de clase (CLSID) como parámetro.</span><span class="sxs-lookup"><span data-stu-id="20165-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="20165-121">Basándose en ese parámetro, este método puede determinar el tipo específico de objeto de generador de clase que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="20165-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="20165-122">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="20165-122">Notes to implementers</span></span>

<span data-ttu-id="20165-123">Puede volver de la implementación de **CreateClassFactory** el mismo objeto de generador de clases en varias llamadas para el mismo identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="20165-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="20165-124">No es necesario crear una nueva instancia de generador de clases.</span><span class="sxs-lookup"><span data-stu-id="20165-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="20165-125">Puede tener una implementación de fábrica de clase única que cree las instancias de fábrica de clases apropiadas a petición o varias implementaciones de fábrica de clases, una para cada clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="20165-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="20165-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="20165-126">See also</span></span>



[<span data-ttu-id="20165-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20165-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

