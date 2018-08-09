---
title: Entradas de lista de las secciones de servicios de mensaje MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cfb06e8dd305add6049d035c44685be047dc744f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818025"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="f6d3d-103">Entradas de lista de las secciones de servicios de mensaje MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="f6d3d-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="f6d3d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6d3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6d3d-105">Hay dos tipos de entradas de la lista sección: uno que se enumeran las secciones de proveedor de servicio y otro que se enumeran en las secciones varios mensajes específicos del servicio.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="f6d3d-106">Estos dos tipos de entradas aparecen en mapisvc.inf con los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="f6d3d-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="f6d3d-107">Cada sección de la entrada de **proveedores** se asigna a una sección individual que proporciona información de configuración para un proveedor de servicio que pertenece al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="f6d3d-108">Cada sección de la entrada de **secciones** se asigna a una sección que contiene información de configuración adicional necesaria para el servicio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="f6d3d-109">Los implementadores de servicio de mensaje definición secciones adicionales cuando desean incluir información especial que no cabe en las secciones estándares.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="f6d3d-110">Servicios de mensaje que hayan complicado configuraciones normalmente use la entrada de **secciones** para agregar información adicional.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="f6d3d-111">Cada sección de servicios de mensaje tiene una entrada de **proveedores** con al menos una sección en la lista; No todas las secciones de servicio de mensaje tienen una entrada de **secciones** .</span><span class="sxs-lookup"><span data-stu-id="f6d3d-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="f6d3d-112">Siguen dos ejemplos de las secciones de servicio de mensaje.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="f6d3d-113">La primera sección es para el servicio de libreta de direcciones predeterminada de la ilustración anterior, un servicio de mensaje sencillo con un proveedor de servicio único.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="f6d3d-114">La segunda sección es para el servicio de MsgService, un servicio de mensajes de ejemplo más complejo con tres proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
```cpp
[AB]
PR_DISPLAY_NAME=Default Address Book
Providers=AB Provider
PR_SERVICE_DLL_NAME=AB.DLL
PR_SERVICE_SUPPORT_FILES=AB.DLL
PR_SERVICE_ENTRY_NAME=DABServiceEntry
PR_RESOURCE_FLAGS=SERVICE_NO_PRIMARY_IDENTITY
[MsgService]
PR_DISPLAY_NAME=My Own Service
Providers=MsgService Prov1, MsgService Prov2, MsgService Prov3
Sections=First_Special_Section, Second_Special_Section
PR_SERVICE_DLL_NAME=MYSERV.DLL
PR_SERVICE_SUPPORT_FILES=MYSERV.DLL, MYXXX.DLL, MYZZZ.DLL
PR_SERVICE_ENTRY_NAME=MyServiceEntry
PR_RESOURCE_FLAGS=SERVICE_SINGLE_COPY
66040003=00000000

```

<span data-ttu-id="f6d3d-115">La entrada de **secciones** en la sección **[MsgService]** enumera dos secciones adicionales, uno llamado **[First_Special_Section]** y la otra denominada **[Second_Special_Section]**.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="f6d3d-116">Los datos que es posible que aparezcan en las secciones adicionales están significativos para el servicio de mensajes específicos.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="f6d3d-117">Estas secciones aparecen siguientes ilustran las secciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="f6d3d-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


