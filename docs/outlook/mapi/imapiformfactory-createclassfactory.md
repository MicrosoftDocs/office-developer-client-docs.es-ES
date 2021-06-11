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
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="4e814-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="4e814-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="4e814-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e814-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e814-105">Devuelve un objeto de fábrica de clase para el formulario.</span><span class="sxs-lookup"><span data-stu-id="4e814-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="4e814-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4e814-106">Parameters</span></span>

 <span data-ttu-id="4e814-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="4e814-107">_clsidForm_</span></span>
  
> <span data-ttu-id="4e814-108">[in] Identificador de clase para el formulario que va a crear la fábrica de clases.</span><span class="sxs-lookup"><span data-stu-id="4e814-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="4e814-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e814-109">_ulFlags_</span></span>
  
> <span data-ttu-id="4e814-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="4e814-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4e814-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="4e814-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="4e814-112">[salida] Puntero al objeto de fábrica de clase.</span><span class="sxs-lookup"><span data-stu-id="4e814-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e814-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e814-113">Return value</span></span>

<span data-ttu-id="4e814-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e814-114">S_OK</span></span> 
  
> <span data-ttu-id="4e814-115">Se ha devuelto el objeto de fábrica de clase.</span><span class="sxs-lookup"><span data-stu-id="4e814-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e814-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e814-116">Remarks</span></span>

<span data-ttu-id="4e814-117">Los visores de formularios llaman al **método IMAPIFormFactory::CreateClassFactory** para obtener una fábrica de clases para un formulario específico.</span><span class="sxs-lookup"><span data-stu-id="4e814-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="4e814-118">La fábrica de clases se usa para crear instancias de un formulario que controla los mensajes de una clase específica y para controlar el acceso a estas instancias.</span><span class="sxs-lookup"><span data-stu-id="4e814-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="4e814-119">Los visores de formularios llaman al método **CreateClassFactory** para obtener un objeto de fábrica de clases para servidores de formulario que implementan varias clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4e814-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="4e814-120">Este método recibe un identificador de clase (CLSID) como parámetro.</span><span class="sxs-lookup"><span data-stu-id="4e814-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="4e814-121">En función de ese parámetro, este método puede determinar el tipo específico de objeto de fábrica de clase que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="4e814-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4e814-122">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4e814-122">Notes to implementers</span></span>

<span data-ttu-id="4e814-123">Puede devolver de la implementación **CreateClassFactory** el mismo objeto de fábrica de clase en varias llamadas para el mismo identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="4e814-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="4e814-124">No es necesario crear una nueva instancia de fábrica de clases.</span><span class="sxs-lookup"><span data-stu-id="4e814-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="4e814-125">Puede tener una implementación de fábrica de una sola clase que cree instancias de fábrica de clases adecuadas a petición, o varias implementaciones de fábrica de clase, una para cada clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="4e814-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e814-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e814-126">See also</span></span>



[<span data-ttu-id="4e814-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e814-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

