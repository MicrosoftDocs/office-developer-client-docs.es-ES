---
title: Información general sobre programación de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: d69d15f0f635c81bea30401b3a6d6e3ccf620112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408344"
---
# <a name="mapi-programming-overview"></a>Información general sobre programación de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta referencia de la API de mensajería de Microsoft Outlook (MAPI) está escrita para desarrolladores de C y C++ con una variedad de necesidades y experiencia con la mensajería. Para los desarrolladores que desean usar MAPI para aumentar sus aplicaciones que tienen características de mensajería, no se requiere ningún conocimiento previo específico. Necesita un fondo en mensajería y el modelo de objetos componentes (COM) para usar MAPI para crear controladores o aplicaciones de grupo de trabajo a escala completa para servicios del sistema de mensajería especializados.
  
Antes de iniciar el trabajo de desarrollo, debe tener en cuenta la siguiente información sobre cómo usar MAPI, el proceso de inicio de sesión y cómo se crean y configuran los perfiles y los servicios de mensajes.
  
La Interfaz de programa de aplicaciones de mensajería (MAPI) es un amplio conjunto de funciones que los programadores pueden usar para crear aplicaciones habilitadas para correo. La biblioteca de funciones completa se conoce como MAPI. MAPI permite un control completo sobre el sistema de mensajería en el equipo cliente, la creación y administración de mensajes, la administración del buzón de cliente, los proveedores de servicios, entre otros.
  
> [!NOTE]
> MAPI extendido es el mismo que MAPI y simplemente se hace referencia a MAPI en la documentación de MAPI. 
  
 **Simple MAPI**
  
Simple MAPI proporciona un conjunto de funciones que le permite agregar un nivel básico de funcionalidad de mensajería a las aplicaciones basadas en Microsoft Windows.
  
> [!IMPORTANT]
> La función MAPI simple MAPISendMail es compatible con Microsoft Outlook 2013 y Microsoft Outlook 2010. Otras funciones MAPI sencillas han quedado en desuso en Windows. 
  

