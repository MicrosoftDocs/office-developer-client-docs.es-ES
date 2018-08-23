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
ms.openlocfilehash: cb5cb5a0169e716f7fcc7f596660bc0222c51c84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572161"
---
# <a name="imapiformfactorycreateclassfactory"></a><span data-ttu-id="a6f26-103">IMAPIFormFactory::CreateClassFactory</span><span class="sxs-lookup"><span data-stu-id="a6f26-103">IMAPIFormFactory::CreateClassFactory</span></span>

  
  
<span data-ttu-id="a6f26-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6f26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6f26-105">Devuelve un objeto de fábrica de clase para el formulario.</span><span class="sxs-lookup"><span data-stu-id="a6f26-105">Returns a class factory object for the form.</span></span>
  
```cpp
HRESULT CreateClassFactory(
  REFCLSID clsidForm,
  ULONG ulFlags,
  LPCLASSFACTORY FAR * lppClassFactory
);
```

## <a name="parameters"></a><span data-ttu-id="a6f26-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6f26-106">Parameters</span></span>

 <span data-ttu-id="a6f26-107">_clsidForm_</span><span class="sxs-lookup"><span data-stu-id="a6f26-107">_clsidForm_</span></span>
  
> <span data-ttu-id="a6f26-108">[entrada] Un identificador de clase para el formulario que se creará la fábrica de clase.</span><span class="sxs-lookup"><span data-stu-id="a6f26-108">[in] A class identifier for the form to be created by the class factory.</span></span>
    
 <span data-ttu-id="a6f26-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6f26-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a6f26-110">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="a6f26-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a6f26-111">_lppClassFactory_</span><span class="sxs-lookup"><span data-stu-id="a6f26-111">_lppClassFactory_</span></span>
  
> <span data-ttu-id="a6f26-112">[out] Un puntero al objeto de fábrica de clase.</span><span class="sxs-lookup"><span data-stu-id="a6f26-112">[out] A pointer to the class factory object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6f26-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6f26-113">Return value</span></span>

<span data-ttu-id="a6f26-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6f26-114">S_OK</span></span> 
  
> <span data-ttu-id="a6f26-115">Se devuelve el objeto de fábrica de clase.</span><span class="sxs-lookup"><span data-stu-id="a6f26-115">The class factory object was returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6f26-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a6f26-116">Remarks</span></span>

<span data-ttu-id="a6f26-117">Visores de formulario llamar al método **IMAPIFormFactory::CreateClassFactory** para obtener un generador de clases para un formulario específico.</span><span class="sxs-lookup"><span data-stu-id="a6f26-117">Form viewers call the **IMAPIFormFactory::CreateClassFactory** method to obtain a class factory for a specific form.</span></span> <span data-ttu-id="a6f26-118">La fábrica de clase se usa para crear instancias de un formulario que controla los mensajes de una clase específica y para controlar el acceso a estas instancias.</span><span class="sxs-lookup"><span data-stu-id="a6f26-118">The class factory is used to create instances of a form that handles messages of a specific class and to control the access to these instances.</span></span> 
  
<span data-ttu-id="a6f26-119">Se llama al método de **CreateClassFactory** por los visores de formulario para obtener un objeto de fábrica de clase para los servidores de formulario que implementan varias clases de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6f26-119">The **CreateClassFactory** method is called by form viewers to obtain a class factory object for form servers that implement multiple message classes.</span></span> <span data-ttu-id="a6f26-120">Este método recibe un identificador de clase (CLSID) como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="a6f26-120">This method receives a class identifier (CLSID) as a parameter.</span></span> <span data-ttu-id="a6f26-121">En función de dicho parámetro, este método puede determinar el tipo específico del objeto de fábrica de clase que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="a6f26-121">Based on that parameter, this method can determine the specific kind of class factory object to return.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a6f26-122">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="a6f26-122">Notes to implementers</span></span>

<span data-ttu-id="a6f26-123">Puede devolver desde la implementación de **CreateClassFactory** el mismo objeto de fábrica de clase en varias llamadas para el mismo identificador de clase.</span><span class="sxs-lookup"><span data-stu-id="a6f26-123">You can return from your **CreateClassFactory** implementation the same class factory object on multiple calls for the same class identifier.</span></span> <span data-ttu-id="a6f26-124">Creación de una nueva instancia de la fábrica de clase no es necesario.</span><span class="sxs-lookup"><span data-stu-id="a6f26-124">Creating a new class factory instance is not required.</span></span> 
  
<span data-ttu-id="a6f26-125">Puede tener una implementación de fábrica de clase único que crea instancias de la fábrica de clase adecuada a petición o varias implementaciones de fábrica de clase, uno para cada clase de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a6f26-125">You can have a single class factory implementation that creates appropriate class factory instances on demand, or multiple class factory implementations, one for each message class.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6f26-126">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a6f26-126">See also</span></span>



[<span data-ttu-id="a6f26-127">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6f26-127">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

