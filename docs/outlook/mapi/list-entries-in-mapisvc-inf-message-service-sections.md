---
title: Entradas de lista de las secciones de servicios de mensaje MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4f052d6-ef63-421a-9d8c-4f3c6df83863
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b6b641a288cea8bac5a1990e85520f3583c02f22
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307836"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Entradas de lista de las secciones de servicios de mensaje MapiSvc. inf

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay dos tipos de entradas de la lista de secciones: una que enumera secciones de proveedores de servicios y otra que enumera secciones de servicios de mensajes varios. Estos dos tipos de entradas aparecen en MAPISVC. inf con los siguientes formatos:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Cada sección de la entrada **proveedores** se asigna a una sección individual que proporciona información de configuración de un proveedor de servicios que pertenece al servicio de mensajes. Cada sección de la entrada de **secciones** se asigna a una sección que contiene información de configuración adicional que necesita el servicio de mensajes. Los implementadores del servicio de mensajes definen secciones adicionales cuando desean incluir información especial que no se ajusta a las secciones estándar. Los servicios de mensajes que tienen configuraciones complicadas normalmente usan la entrada de **secciones** para agregar información adicional. Cada sección de servicios de mensajes tiene una entrada de **proveedores** con al menos una sección de la lista; no todas las secciones de servicio de mensajes tienen una entrada de **secciones** . 
  
A continuación, se muestran dos ejemplos de secciones de servicio de mensajes. La primera sección es para el servicio de libreta de direcciones predeterminado de la ilustración anterior, un servicio de mensajes sencillo con un solo proveedor de servicios. La segunda sección es para el servicio de MsgService, un servicio de mensajes de ejemplo más complejo con tres proveedores de servicios. 
  
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

La entrada de **secciones** de la sección **[MsgService]** muestra dos secciones adicionales, una llamada **[First_Special_Section]** y otra llamada **[Second_Special_Section]**. Los datos que pueden aparecer en secciones adicionales son significativos para el servicio de mensajes específico. Estas secciones se muestran a continuación para ilustrar secciones adicionales. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


