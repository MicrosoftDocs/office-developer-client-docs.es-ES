---
title: Constantes (API exportadas de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Este tema contiene definiciones de constantes para las API que exporta Outlook.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319876"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="bccdd-103">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="bccdd-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="bccdd-104">Este tema contiene definiciones de constantes para las API que exporta Outlook.</span><span class="sxs-lookup"><span data-stu-id="bccdd-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="bccdd-105">Definiciones de compatibilidad con zona horaria</span><span class="sxs-lookup"><span data-stu-id="bccdd-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="bccdd-106">Definiciones para compatibilidad con categorías</span><span class="sxs-lookup"><span data-stu-id="bccdd-106">Definitions for Category support</span></span>

|<span data-ttu-id="bccdd-107">**Constante**</span><span class="sxs-lookup"><span data-stu-id="bccdd-107">**Constant**</span></span>|<span data-ttu-id="bccdd-108">**Definición**</span><span class="sxs-lookup"><span data-stu-id="bccdd-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bccdd-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="bccdd-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="bccdd-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bccdd-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="bccdd-111">Identificadores de distribución varios</span><span class="sxs-lookup"><span data-stu-id="bccdd-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="bccdd-112">Outlook expone los siguientes identificadores de envío (dispids) para que los desarrolladores puedan usar [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) para tener acceso a la propiedad o método correspondiente, o escuchar el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="bccdd-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="bccdd-113">**Constante asociada**</span><span class="sxs-lookup"><span data-stu-id="bccdd-113">**Associated constant**</span></span>|<span data-ttu-id="bccdd-114">**Valor insípido**</span><span class="sxs-lookup"><span data-stu-id="bccdd-114">**Dispid value**</span></span>|<span data-ttu-id="bccdd-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bccdd-115">**Description**</span></span>|<span data-ttu-id="bccdd-116">**Interfaz aplicable**</span><span class="sxs-lookup"><span data-stu-id="bccdd-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bccdd-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="bccdd-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="bccdd-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="bccdd-118">0xF024</span></span>  <br/> |<span data-ttu-id="bccdd-119">Se usa para invocar la propiedad correspondiente en un elemento para comprobar si el elemento se ha modificado pero no se ha guardado.</span><span class="sxs-lookup"><span data-stu-id="bccdd-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="bccdd-120">Objetos de nivel de elemento</span><span class="sxs-lookup"><span data-stu-id="bccdd-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="bccdd-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="bccdd-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="bccdd-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="bccdd-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="bccdd-123">Se usa para invocar el método correspondiente en el explorador o inspector para especificar si se va a mostrar la imagen de un contacto, basándose en un argumento determinado.</span><span class="sxs-lookup"><span data-stu-id="bccdd-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="bccdd-124">Explorador o inspector</span><span class="sxs-lookup"><span data-stu-id="bccdd-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="bccdd-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="bccdd-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="bccdd-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="bccdd-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="bccdd-127">Se usa para controlar el evento de la **función IDispatch::Invoke** que se ejecuta antes de una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="bccdd-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="bccdd-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bccdd-128">Application</span></span>  <br/> |
|<span data-ttu-id="bccdd-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="bccdd-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="bccdd-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="bccdd-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="bccdd-131">Se usa para controlar el evento de la **función IDispatch::Invoke** que se ejecuta cuando Outlook ha completado la lectura de las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="bccdd-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="bccdd-132">Objetos de nivel de elemento</span><span class="sxs-lookup"><span data-stu-id="bccdd-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bccdd-133">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bccdd-133">See also</span></span>

- [<span data-ttu-id="bccdd-134">API exportadas de Outlook</span><span class="sxs-lookup"><span data-stu-id="bccdd-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="bccdd-135">Información sobre las API exportadas por Outlook</span><span class="sxs-lookup"><span data-stu-id="bccdd-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="bccdd-136">Determinar si un elemento de Outlook se ha modificado pero no guardado (referencia auxiliar de Outlook)</span><span class="sxs-lookup"><span data-stu-id="bccdd-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="bccdd-137">Especificar si se debe mostrar la imagen de un contacto en Outlook (referencia auxiliar de Outlook)</span><span class="sxs-lookup"><span data-stu-id="bccdd-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [<span data-ttu-id="bccdd-138">Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="bccdd-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

