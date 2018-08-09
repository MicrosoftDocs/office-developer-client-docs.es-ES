---
title: Informaci�n general sobre programaci�n de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 177bd84addb001970e52801fd2cddba3a8d81706
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818168"
---
# <a name="mapi-programming-overview"></a>Informaci�n general sobre programaci�n de MAPI

  
  
**Hace referencia a**: Outlook 
  
Esta referencia de API de mensajería de Outlook (MAPI) de Microsoft se ha diseñado para C y los desarrolladores de C++ con una gran variedad de necesidades y experimentar con la mensajería. Para los programadores que deseen utilizar MAPI para ampliar sus aplicaciones que tienen las características de mensajería, no es necesario ningún requisito de conocimientos específico. Es necesario un fondo de mensajería y el modelo de objetos de componentes (COM) a usar MAPI para crear aplicaciones de grupo de trabajo a gran escala o controladores para los servicios del sistema de mensajería especializados.
  
Antes de iniciar el trabajo de desarrollo, debe tener en cuenta la siguiente información acerca de cómo usar MAPI, el proceso de inicio de sesión, y cómo se crean y configuran perfiles y servicios de mensajes.
  
La interfaz de programa de aplicaciones de mensajería (MAPI) es un amplio conjunto de funciones que pueden usar los desarrolladores para crear aplicaciones habilitadas para correo. La biblioteca de función completa se conoce como MAPI. MAPI permite el control completo sobre el sistema de mensajería en el equipo cliente, la creación y la administración de los mensajes, la administración de los buzones de correo de cliente, proveedores de servicios y así sucesivamente.
  
> [!NOTE]
> MAPI extendida es el mismo que MAPI y se simplemente denomina MAPI en la documentación de MAPI. 
  
 **Simple MAPI**
  
Simple MAPI proporciona un conjunto de funciones que permite agregar un nivel básico de funcionalidad de mensajería a las aplicaciones basadas en Windows de Microsoft.
  
> [!IMPORTANT]
> La función de Simple MAPI MAPISendMail es compatible con Microsoft Outlook 2013 y Microsoft Outlook 2010. Otras funciones de Simple MAPI han quedado obsoletos en Windows. 
  

