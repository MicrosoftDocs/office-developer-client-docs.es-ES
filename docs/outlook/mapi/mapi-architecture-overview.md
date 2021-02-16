---
title: Introducción a la arquitectura MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410080"
---
# <a name="mapi-architecture-overview"></a>Introducción a la arquitectura MAPI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI define una arquitectura modular, como se muestra en la siguiente ilustración.  
  
![Arquitectura de Outlook 2010](media/amapi_43.gif "Arquitectura de Outlook 2010")
  
La aplicación MAPI se conoce como aplicación cliente porque es un cliente del subsistema MAPI. Las aplicaciones basadas en mensajería emplean la mensajería como parte central de su procesamiento y ofrecen amplias características de mensajería, como el intercambio de información de varios tipos en varios formatos y la capacidad de guardar y organizar la información localmente. Las aplicaciones de flujo de trabajo, programación y correo electrónico son ejemplos de aplicaciones basadas en mensajería.
  
El subsistema MAPI está configurado por una interfaz de usuario común y las interfaces de programación. La interfaz de usuario común es un conjunto de cuadros de diálogo que ofrece a las aplicaciones cliente una apariencia coherente y a los usuarios una forma coherente de trabajar.
  
MAPI tiene interfaces de programación que usan el subsistema MAPI, los programadores de software cliente y los desarrolladores de proveedores de servicios. La interfaz de programación MAPI es la interfaz de programación principal basada en objetos. La interfaz de programación MAPI es similar al modelo de objetos de componentes OLE y la usan el subsistema MAPI y las aplicaciones cliente basadas en mensajería escritas en C o C++. 
  
Como desarrollador de software cliente, realiza llamadas MAPI directamente a través de la interfaz de programación MAPI. Puede implementar la mensajería con una única interfaz de cliente MAPI o una combinación de interfaces. Una sola aplicación puede realizar llamadas a métodos o funciones pertenecientes a cualquiera de las interfaces.
  
## <a name="see-also"></a>Consulte también

-[Arquitectura y características mapi](mapi-features-and-architecture.md)

