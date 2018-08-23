---
title: Información general sobre la característica MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 034f3dd8bc68462348bc92a8acf2904ab66fc798
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575612"
---
# <a name="mapi-feature-overview"></a>Información general sobre la característica MAPI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI tiene varias características claves que le permiten proporcionar una manera coherente para desarrolladores trabajar con y utilizar distintos sistemas de mensajería en forma transparente. Estas características incluyen una completa y abrir la interfaz de programación y compatibilidad con los estándares del sector. 
  
Dado que MAPI es una interfaz de programación de open, proporciona servicios de forma genérica, lo que permite a los usuarios agregar cualquier personalización necesario ahora y en el futuro. La interfaz de programación de MAPI cumple los requisitos de aplicaciones de cliente con diversas necesidades de mensajería, como una aplicación de procesamiento de textos que requiere sólo la capacidad de enviar documentos o una aplicación de grupo de trabajo que requiere la capacidad de compartir y almacenar distintos tipos de datos. De hecho, todas las aplicaciones que necesita para exchange o para almacenar información en un formato determinado pueden beneficiarse de la interfaz de programación de MAPI. Cualquier proveedor de servicios puede usar la interfaz para exponer las características exclusivas de su sistema de mensajería, selección de esas características que proporcionan el máximo provecho a los usuarios de la aplicación.
  
MAPI proporciona separación entre la interfaz de programación utilizada por las aplicaciones de cliente de mensajería de front-end y la interfaz de programación utilizada por los proveedores de servicios back-end. Separación de la interfaz de cliente desde el proveedor de servicios permite que una sola aplicación utilizar varios sistemas de mensajería y varias aplicaciones para usar un proveedor de servicio único. Cada componente funciona con una interfaz de usuario basada en Windows de Microsoft comunes. Esto es una gran ventaja para los usuarios. Los usuarios pueden seleccionar desde una variedad de sistemas, dependiendo de sus necesidades en cualquier momento y pueden funcionan de manera coherente con cada sistema seleccionado, lo que proporciona independencia true desde sistemas de mensajería específicos. 
  
Por ejemplo, una sola aplicación de cliente de mensajería puede recibir mensajes de fax, correo de voz y una fuente RSS. Los mensajes de todos estos sistemas se pueden colocar en una sola ubicación o universal Bandeja de entrada, en la llegada. Tener una sola aplicación controlar todos estos sistemas, reduce el costo de desarrollo, el aprendizaje del usuario y la administración del sistema. 
  
Separación de la interfaz de cliente de la interfaz del proveedor quita las dependencias de programación colocadas en la aplicación mediante el sistema de mensajería y viceversa. Los desarrolladores de aplicaciones de cliente y proveedores de servicios de escriben código para un conjunto estándar de funciones MAPI, en lugar de un conjunto diverso de características específicas del sistema específicos de la aplicación o de mensajería. Los programadores centrarse sólo en su componente, si es un proveedor de servicio o cliente y MAPI encarga del resto, lo que reduce los costos y tiempo de desarrollo.
  
La interfaz de programación de MAPI proporciona un completo conjunto de características. MAPI está dirigida a profesionales del mercado nuevo eficaces de aplicaciones de grupo de trabajo, las aplicaciones que se comunican con esos distintos sistemas de mensajería como fax, DEC All-In-1, correo de voz y servicios de comunicaciones públicas como AT & T Easylink servicios, CompuServe y MCI CORREO. La interfaz MAPI permite a los proveedores de servicio debe estar disponible para todos estos sistemas. 
  
Objetos compatible con MAPI son similares en el formulario a los objetos del modelo de objetos componentes (COM). Objetos COM implementan un conjunto de métodos que pertenecen a una o más interfaces o colecciones de funciones relacionadas que definen cómo se comportan los objetos y a operan en COM. Los usuarios tener acceso a los objetos COM sólo a través de punteros a estas interfaces.
  
MAPI proporciona compatibilidad multiplataforma a través de dichos estándares del sector como SMTP y X.400. Puede ejecutar las aplicaciones MAPI en Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 y Windows XP. 
  
## <a name="see-also"></a>Recursos adicionales

- [Arquitectura y las características MAPI](mapi-features-and-architecture.md)

