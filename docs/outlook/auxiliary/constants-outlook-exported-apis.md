---
title: Constantes (API exportadas de Outlook)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Este tema contiene las definiciones de constantes para las API que exporta de Outlook.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386078"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="42d0b-103">Constantes (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="42d0b-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="42d0b-104">Este tema contiene las definiciones de constantes para las API que exporta de Outlook.</span><span class="sxs-lookup"><span data-stu-id="42d0b-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="42d0b-105">Admiten las definiciones de zona horaria</span><span class="sxs-lookup"><span data-stu-id="42d0b-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="42d0b-106">Definiciones de soporte de categoría</span><span class="sxs-lookup"><span data-stu-id="42d0b-106">Definitions for Category support</span></span>

|<span data-ttu-id="42d0b-107">**Constante**</span><span class="sxs-lookup"><span data-stu-id="42d0b-107">**Constant**</span></span>|<span data-ttu-id="42d0b-108">**Definición**</span><span class="sxs-lookup"><span data-stu-id="42d0b-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="42d0b-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="42d0b-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="42d0b-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="42d0b-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="42d0b-111">Identificadores de envío varios</span><span class="sxs-lookup"><span data-stu-id="42d0b-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="42d0b-112">Outlook expone los siguientes identificadores de envío (DISPID) para que los programadores pueden utilizar [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) para obtener acceso a la propiedad correspondiente o el método o escuchar el evento correspondiente.</span><span class="sxs-lookup"><span data-stu-id="42d0b-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="42d0b-113">**Constante asociada**</span><span class="sxs-lookup"><span data-stu-id="42d0b-113">**Associated constant**</span></span>|<span data-ttu-id="42d0b-114">**Valor de DISPID**</span><span class="sxs-lookup"><span data-stu-id="42d0b-114">**Dispid value**</span></span>|<span data-ttu-id="42d0b-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="42d0b-115">**Description**</span></span>|<span data-ttu-id="42d0b-116">**Interfaz aplicable**</span><span class="sxs-lookup"><span data-stu-id="42d0b-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="42d0b-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="42d0b-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="42d0b-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="42d0b-118">0xF024</span></span>  <br/> |<span data-ttu-id="42d0b-119">Se usa para invocar la propiedad correspondiente en un elemento para comprobar si el elemento se ha modificado pero no se ha guardado.</span><span class="sxs-lookup"><span data-stu-id="42d0b-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="42d0b-120">Objetos de nivel de elemento</span><span class="sxs-lookup"><span data-stu-id="42d0b-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="42d0b-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="42d0b-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="42d0b-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="42d0b-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="42d0b-123">Se usa para invocar el método correspondiente en el explorador o inspector para especificar si se debe mostrar la imagen de un contacto, basándose en un argumento determinado.</span><span class="sxs-lookup"><span data-stu-id="42d0b-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="42d0b-124">El explorador o inspector</span><span class="sxs-lookup"><span data-stu-id="42d0b-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="42d0b-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="42d0b-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="42d0b-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="42d0b-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="42d0b-127">Se usa para controlar el evento de la función de **IDispatch:: Invoke** que se desencadena antes de una operación de impresión.</span><span class="sxs-lookup"><span data-stu-id="42d0b-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="42d0b-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="42d0b-128">Application</span></span>  <br/> |
|<span data-ttu-id="42d0b-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="42d0b-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="42d0b-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="42d0b-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="42d0b-131">Se usa para controlar el evento de la función de **IDispatch:: Invoke** que se desencadena cuando Outlook ha finalizado la lectura de las propiedades del elemento.</span><span class="sxs-lookup"><span data-stu-id="42d0b-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="42d0b-132">Objetos de nivel de elemento</span><span class="sxs-lookup"><span data-stu-id="42d0b-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42d0b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="42d0b-133">See also</span></span>

- [<span data-ttu-id="42d0b-134">API exportadas de Outlook</span><span class="sxs-lookup"><span data-stu-id="42d0b-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="42d0b-135">Información sobre las API exportadas por Outlook</span><span class="sxs-lookup"><span data-stu-id="42d0b-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="42d0b-136">Determinar si un elemento de Outlook se ha modificado pero no guardado (referencia auxiliar de Outlook)</span><span class="sxs-lookup"><span data-stu-id="42d0b-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="42d0b-137">Especificar si se debe mostrar la imagen de un contacto en Outlook (referencia auxiliar de Outlook)</span><span class="sxs-lookup"><span data-stu-id="42d0b-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [<span data-ttu-id="42d0b-138">Los eventos disponibles y su identificadores DispId (API exportadas de Outlook)</span><span class="sxs-lookup"><span data-stu-id="42d0b-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

