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
ms.openlocfilehash: c5b5c468b56e5b34d265e7f00bbee96142a88e1c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591124"
---
# <a name="list-entries-in-mapisvcinf-message-service-sections"></a>Entradas de lista de las secciones de servicios de mensaje MapiSvc.inf

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Hay dos tipos de entradas de la lista sección: uno que se enumeran las secciones de proveedor de servicio y otro que se enumeran en las secciones varios mensajes específicos del servicio. Estos dos tipos de entradas aparecen en mapisvc.inf con los siguientes formatos:
  
```cpp
Providersprovider section1, provider section2, ...... provider sectionX
Sectionssection name1, section name2, ......section nameX

```

Cada sección de la entrada de **proveedores** se asigna a una sección individual que proporciona información de configuración para un proveedor de servicio que pertenece al servicio de mensajes. Cada sección de la entrada de **secciones** se asigna a una sección que contiene información de configuración adicional necesaria para el servicio de mensaje. Los implementadores de servicio de mensaje definición secciones adicionales cuando desean incluir información especial que no cabe en las secciones estándares. Servicios de mensaje que hayan complicado configuraciones normalmente use la entrada de **secciones** para agregar información adicional. Cada sección de servicios de mensaje tiene una entrada de **proveedores** con al menos una sección en la lista; No todas las secciones de servicio de mensaje tienen una entrada de **secciones** . 
  
Siguen dos ejemplos de las secciones de servicio de mensaje. La primera sección es para el servicio de libreta de direcciones predeterminada de la ilustración anterior, un servicio de mensaje sencillo con un proveedor de servicio único. La segunda sección es para el servicio de MsgService, un servicio de mensajes de ejemplo más complejo con tres proveedores de servicios. 
  
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

La entrada de **secciones** en la sección **[MsgService]** enumera dos secciones adicionales, uno llamado **[First_Special_Section]** y la otra denominada **[Second_Special_Section]**. Los datos que es posible que aparezcan en las secciones adicionales están significativos para el servicio de mensajes específicos. Estas secciones aparecen siguientes ilustran las secciones adicionales. 
  
```cpp
[First_Special_Section]
UID=13DB0C8AA05101A9BB000AA002FC45A
66020003=01000000
66000003=00040000
66010003=06000000
66050003=03000000

```


