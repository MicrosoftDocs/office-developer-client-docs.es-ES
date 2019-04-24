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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297896"
---
# <a name="mapi-architecture-overview"></a>Introducción a la arquitectura MAPI
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
MAPI define una arquitectura modular, tal como se muestra en la siguiente ilustración.  
  
![Arquitectura de Outlook 2010] (media/amapi_43.gif "Arquitectura de Outlook 2010")
  
La aplicación MAPI se conoce como una aplicación cliente porque es un cliente del subsistema MAPI. Las aplicaciones basadas en mensajería usan la mensajería como parte central de su procesamiento y ofrecen amplias características de mensajería, como el intercambio de información de distintos tipos en distintos formatos y la capacidad de guardar y organizar la información de forma local. Las aplicaciones de correo electrónico, programación y flujo de trabajo son ejemplos de aplicaciones basadas en mensajería.
  
El subsistema MAPI consta de una interfaz de usuario común y de las interfaces de programación. La interfaz de usuario común es un conjunto de cuadros de diálogo que da a las aplicaciones cliente un aspecto coherente y a los usuarios una forma coherente de trabajar.
  
MAPI tiene interfaces de programación usadas por el subsistema MAPI, por desarrolladores de software de cliente y por programadores de proveedores de servicios. La interfaz de programación de MAPI es la interfaz de programación basada en objetos principal. La interfaz de programación de MAPI es similar al modelo de objetos de componentes OLE y se usa en el subsistema MAPI y en las aplicaciones cliente basadas en mensajería escritas en C o C++. 
  
Como desarrollador de software de cliente, realiza llamadas MAPI directamente a través de la interfaz de programación MAPI. Puede implementar la mensajería con una única interfaz de cliente MAPI o con una combinación de interfaces. Una sola aplicación puede realizar llamadas a métodos o funciones pertenecientes a cualquiera de las interfaces.
  
## <a name="see-also"></a>Vea también

-[Arquitectura y características de MAPI](mapi-features-and-architecture.md)

