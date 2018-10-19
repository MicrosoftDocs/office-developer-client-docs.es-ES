---
title: Información sobre cómo establecer el orden de resolución de las listas de direcciones en Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: 07a4c3e90f686f291f95ff87f337b54d8bf35edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391412"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>Información sobre cómo establecer el orden de resolución de las listas de direcciones en Outlook

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Para cada perfil, Microsoft Office Outlook admite varias listas de direcciones y los usuarios pueden especificar manualmente el orden de las listas de direcciones por las que se resuelven los destinatarios de correo electrónico y los asistentes de las convocatorias de reunión. Por ejemplo, puede establecer el orden de resolución para que los nombres se resuelvan primero en la libreta de direcciones de Outlook y, a continuación, en la lista Global de direcciones. En un ordenador, un usuario puede abrir la libreta de direcciones, hacer clic en **Herramientas** y **Opciones** para especificar el orden de resolución. Sin embargo, en un entorno corporativo, es más eficaz que los administradores de TI establezcan mediante programación el orden de las listas de direcciones por las que se resuelven los nombres. Dicho código puede usarse como parte de un script de automatización de inicio que un administrador implemente en la organización. 
  
MAPI es compatible con el método **[SetSearchPath](iaddrbook-getsearchpath.md)** de la interfaz **[IAddrBook](iaddrbookimapiprop.md)**, que le permite establecer una nueva ruta de búsqueda en el perfil que se usa para la resolución de nombres. Para usar el método **IAddrBook::SetSearchPath**, debe especificar el orden de resolución deseado a través de una matriz que contiene los contenedores de las libretas de direcciones relevantes en el orden en que deben resolverse. Cada entrada de la matriz también debe contener el identificador de entrada de la libreta de direcciones correspondiente. 
  
Los siguientes son ejemplos de código sobre cómo especificar una ruta de búsqueda personalizada para las listas de direcciones.
  
- [Establecer mediante programación el orden de resolución para las listas de direcciones](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590: Cómo cambiar el orden de clasificación de la libreta de direcciones con SetSearchPath](https://support.microsoft.com/kb/292590)
    

