---
title: Acerca de c�mo establecer el orden de resoluci�n para las listas de direcciones en Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1589568-cb49-86dd-5d16-b08c8117bd17
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 22d56ffac5d9d628b04e364fa772ddc8de488a31
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578657"
---
# <a name="about-setting-the-resolution-order-for-address-lists-in-outlook"></a>Acerca de c�mo establecer el orden de resoluci�n para las listas de direcciones en Outlook

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para cada perfil, Microsoft Office Outlook es compatible con varias listas de direcciones y los usuarios pueden especificar manualmente el orden de las listas de direcciones por qué los destinatarios de correo electrónico se resuelven los mensajes y los asistentes de las convocatorias de reunión. Por ejemplo, puede establecer el orden de resoluci�n para que los nombres se resuelven primero en su libreta de direcciones de Outlook y a continuaci�n, en la lista Global de direcciones. En un equipo, un usuario puede abrir la libreta de direcciones, haga clic en **Herramientas** y, a continuaci�n, en **Opciones** para especificar el orden de resoluci�n. Sin embargo, en un entorno corporativo, es m�s eficaz para los administradores de TI establecer mediante programaci�n el orden de las listas de direcciones mediante el cual se resuelven nombres. Este c�digo puede utilizarse como parte de una secuencia de comandos de automatizaci�n de inicio que un administrador implementa dentro de la corporaci�n. 
  
MAPI es compatible con el m�todo **[SetSearchPath](iaddrbook-getsearchpath.md)** en la interfaz **[IAddrBook](iaddrbookimapiprop.md)**, que le permite establecer una nueva ruta de b�squeda en el perfil que se usa para la resoluci�n de nombres. Para usar el m�todo **IAddrBook::SetSearchPath**, debe especificar el orden de resoluci�n que desee mediante el uso de una matriz que contiene los contenedores de la direcci�n relevante de libros en el orden en que se deben resolver. Cada entrada de la matriz tambi�n debe contener el identificador de entrada de la libreta de direcciones correspondiente. 
  
Los siguientes son ejemplos de c�digo de c�mo especificar una ruta de acceso de b�squeda personalizada para las listas de direcciones.
  
- [Establecer mediante programación el orden de resolución para las listas de direcciones](how-to-programmatically-set-the-resolution-order-for-address-lists.md)
    
- [KB 292590: c�mo cambiar el orden de ordenaci�n de la libreta de direcciones con SetSearchPath](http://support.microsoft.com/kb/292590)
    

