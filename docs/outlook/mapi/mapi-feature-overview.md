---
title: Introducción a la característica MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: b1087f5156ad79b20eb31ef55c0388ffd82e1601
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416926"
---
# <a name="mapi-feature-overview"></a>Introducción a la característica MAPI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI tiene varias características clave que le permiten proporcionar una forma coherente para que los desarrolladores trabajen con y usen diferentes sistemas de mensajería de forma fluida. Estas características incluyen una interfaz de programación completa y abierta y compatibilidad con los estándares del sector. 
  
Dado que MAPI es una interfaz de programación abierta, proporciona servicios de forma genérica, lo que permite a los usuarios agregar cualquier personalización necesaria ahora y en el futuro. La interfaz de programación MAPI cumple los requisitos de las aplicaciones cliente con diversas necesidades de mensajería, como una aplicación de procesamiento de texto que solo requiere la capacidad de enviar documentos o una aplicación de grupo de trabajo que requiere la capacidad de compartir y almacenar diferentes tipos de datos. De hecho, cualquier aplicación que necesite intercambiar o almacenar información en un formato determinado puede beneficiarse de la interfaz de programación MAPI. Cualquier proveedor de servicios puede usar la interfaz para exponer las características únicas de su sistema de mensajería, seleccionando aquellas características que proporcionan la mayor ventaja a los usuarios de la aplicación.
  
MAPI proporciona separación entre la interfaz de programación usada por las aplicaciones cliente de mensajería front-end y la interfaz de programación usada por los proveedores de servicios back-end. La separación de la interfaz de cliente del proveedor de servicios permite que una sola aplicación use varios sistemas de mensajería y varias aplicaciones para usar un único proveedor de servicios. Cada componente funciona con una interfaz de usuario común basada Windows Microsoft. Esto es una gran ventaja para los usuarios. Los usuarios pueden seleccionar entre una variedad de sistemas, según sus necesidades en cualquier momento, y pueden trabajar de forma coherente con cada sistema seleccionado, lo que proporciona una verdadera independencia de sistemas de mensajería específicos. 
  
Por ejemplo, una aplicación cliente de mensajería única puede recibir mensajes de un fax, correo de voz y una fuente RSS. Los mensajes de todos estos sistemas se pueden colocar en una única ubicación, o bandeja de entrada universal, a la llegada. Tener una sola aplicación que controle todos estos sistemas disminuirá el costo de desarrollo, aprendizaje de usuarios y administración del sistema. 
  
La separación de la interfaz de cliente de la interfaz del proveedor quita todas las dependencias de programación que el sistema de mensajería coloca en la aplicación y viceversa. Los desarrolladores de aplicaciones cliente y proveedores de servicios escriben código en un conjunto estándar de características MAPI, en lugar de un conjunto diverso de características específicas de la aplicación o del sistema de mensajería. Los desarrolladores solo se centran en su componente, ya sea un cliente o un proveedor de servicios, y MAPI controla el resto, lo que reduce el tiempo y los costos de desarrollo.
  
La interfaz de programación MAPI proporciona un conjunto completo de características. MAPI está dirigido al nuevo y eficaz mercado de aplicaciones de grupo de trabajo, aplicaciones que se comunican con sistemas de mensajería tan diferentes como fax, DEC All-In-1, correo de voz y servicios de comunicaciones públicas como AT&T Easylink Services, CompuServe y MCI MAIL. La interfaz MAPI permite que los proveedores de servicios estén disponibles para todos estos sistemas. 
  
Los objetos compatibles con MAPI tienen una forma similar a los objetos del modelo de objetos componentes (COM). Los objetos COM implementan un conjunto de métodos que pertenecen a una o más interfaces o colecciones de funciones relacionadas que definen el comportamiento y funcionamiento de los objetos en COM. Los usuarios solo tienen acceso a objetos COM a través de punteros a estas interfaces.
  
MAPI proporciona compatibilidad multiplataforma a través de estándares del sector como SMTP y X.400. Puede ejecutar aplicaciones MAPI en Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 y Windows XP. 
  
## <a name="see-also"></a>Vea también

- [Características y arquitectura MAPI](mapi-features-and-architecture.md)

