---
title: Enumerar entradas en las secciones del servicio de mensajes MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435932"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="9e44b-103">Enumerar entradas en las secciones del servicio de mensajes MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="9e44b-103">List Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="9e44b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e44b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e44b-105">Hay dos tipos de entradas de lista de secciones: una que enumera las secciones del proveedor de servicios y otra que enumera las secciones específicas del servicio de mensajes varios.</span><span class="sxs-lookup"><span data-stu-id="9e44b-105">There are two types of section list entries: one that lists service provider sections and one that lists miscellaneous message service-specific sections.</span></span> <span data-ttu-id="9e44b-106">Estos dos tipos de entradas aparecen en mapisvc.inf con los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="9e44b-106">These two types of entries appear in mapisvc.inf using the following formats:</span></span>
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

<span data-ttu-id="9e44b-107">Cada sección de la entrada **Proveedores** se asigna a una sección individual que proporciona información de configuración para un proveedor de servicios que pertenece al servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9e44b-107">Each section in the **Providers** entry maps to an individual section providing configuration information for a service provider that belongs to the message service.</span></span> <span data-ttu-id="9e44b-108">Cada sección de la **entrada Secciones se** asigna a una sección que contiene información de configuración adicional necesaria para el servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9e44b-108">Each section in the **Sections** entry maps to a section that contains extra configuration information needed by the message service.</span></span> <span data-ttu-id="9e44b-109">Los implementadores del servicio de mensajes definen secciones adicionales cuando desean incluir información especial que no cabe en las secciones estándar.</span><span class="sxs-lookup"><span data-stu-id="9e44b-109">Message service implementers define extra sections when they want to include special information that does not fit in the standard sections.</span></span> <span data-ttu-id="9e44b-110">Los servicios de mensajes que tienen configuraciones complicadas suelen usar **la entrada Secciones** para agregar información adicional.</span><span class="sxs-lookup"><span data-stu-id="9e44b-110">Message services that have complicated configurations typically use the **Sections** entry to add extra information.</span></span> <span data-ttu-id="9e44b-111">Cada sección de servicios de mensajes tiene **una entrada** Proveedores con al menos una sección en la lista; No todas las secciones del servicio de mensajes tienen **una entrada Sections.**</span><span class="sxs-lookup"><span data-stu-id="9e44b-111">Every message services section has a **Providers** entry with at least one section in the list; not all message service sections have a **Sections** entry.</span></span> 
  
<span data-ttu-id="9e44b-112">A continuación se muestran dos ejemplos de secciones de servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="9e44b-112">Two examples of message service sections follow.</span></span> <span data-ttu-id="9e44b-113">La primera sección es para el servicio de libreta de direcciones predeterminado de la ilustración anterior, un servicio de mensajes sencillo con un único proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="9e44b-113">The first section is for the Default Address Book service from the earlier illustration, a straightforward message service with a single service provider.</span></span> <span data-ttu-id="9e44b-114">La segunda sección es para el servicio MsgService, un servicio de mensajes de ejemplo más complejo con tres proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="9e44b-114">The second section is for the MsgService service, a more complex sample message service with three service providers.</span></span> 
  
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

<span data-ttu-id="9e44b-115">La **entrada Secciones** de la sección **[MsgService]** enumera dos secciones adicionales, una llamada **[First_Special_Section]** y la otra llamada **[Second_Special_Section].**</span><span class="sxs-lookup"><span data-stu-id="9e44b-115">The **Sections** entry in the **[MsgService]** section lists two additional sections, one called **[First_Special_Section]** and the other called **[Second_Special_Section]**.</span></span> <span data-ttu-id="9e44b-116">Los datos que pueden aparecer en secciones adicionales son significativos para el servicio de mensajes específico.</span><span class="sxs-lookup"><span data-stu-id="9e44b-116">The data that might appear in extra sections is meaningful to the specific message service.</span></span> <span data-ttu-id="9e44b-117">Estas secciones aparecen a continuación para ilustrar secciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="9e44b-117">These sections appear following to illustrate extra sections.</span></span> 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


