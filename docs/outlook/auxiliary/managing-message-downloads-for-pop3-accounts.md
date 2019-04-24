---
title: Descargas de mensaje administración de las cuentas POP3
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: b4218aa6-1591-49db-9782-f286135fc79a
description: Esta sección describe cómo el proveedor de POP3 de Outlook utiliza el historial de listado de ID único (UIDL) de una cuenta POP3 para identificar los mensajes que el proveedor ha descargado o se eliminan del servidor POP3, para evitar descargar el mismo mensaje más de una vez.
ms.openlocfilehash: 35c50d83c317ebefa52fd9bfcb348c8411a06f25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322249"
---
# <a name="managing-message-downloads-for-pop3-accounts"></a>Descargas de mensaje administración de las cuentas POP3

Esta sección describe cómo el proveedor de POP3 de Outlook utiliza el historial de listado de ID único (UIDL) de una cuenta POP3 para identificar los mensajes que el proveedor ha descargado o se eliminan del servidor POP3, para evitar descargar el mismo mensaje más de una vez.
  
## <a name="introduction-to-pop"></a>Introducción a POP

El protocolo de oficina de correos (POP) especifica un protocolo de capa de aplicación para un cliente de correo electrónico como Outlook descargar mensajes de correo electrónico de un servidor de correo. Permite al usuario descargar una copia de un mensaje de correo electrónico en un dispositivo local (como un teléfono inteligente o equipo) y tampoco deja una copia en el servidor o eliminarlo. El protocolo admite sólo un cliente de correo electrónico para conectarse al buzón a la vez. Especifica cómo recuperar pero no enviar mensajes de correo electrónico desde el servidor de correo. Cuando se utiliza POP, un cliente de correo normalmente tiene que comprobar si hay mensajes nuevos de correo electrónico, se conecta al servidor de correo para que sólo la cantidad de tiempo que se tarda en descargar los mensajes nuevos y no permanecer conectado al servidor para obtener notificaciones de correo nuevo. POP admite sólo los mensajes de correo electrónico pero no otros tipos de elementos como contactos y citas a menos que se encapsulan en un correo electrónico. POP3 es la versión 3 del protocolo.
  
Los mensajes de una cuenta POP se identifican mediante identificadores únicos (UID). Un cliente de correo electrónico que deja el correo en el servidor, utiliza el comando UIDL para recuperar el mapa UIDL que asocia cada mensaje que se ha entregado en el buzón para su UID. El cliente también obtiene el historial UIDL para los mensajes que se han descargado o eliminado de la Bandeja de entrada de ese cliente. Basándose en los antecedentes UIDL, el cliente puede determinar qué mensajes son nuevos y se deben descargar.

- [Buscar el historial de descarga de mensajes de una cuenta POP3](locating-the-message-download-history-for-a-pop3-account.md): en este tema se describe cómo obtiene acceso un cliente de correo a la propiedad [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) para obtener el historial de UIDL para los mensajes de la bandeja de entrada del cliente de una cuenta POP3. 
    
- [Analizar el historial de descarga de mensajes para una cuenta POP3](parsing-the-message-download-history-for-a-pop3-account.md): en este tema se describe cómo analizar el objeto binario POP3 que representa el historial de UIDL para los mensajes de la bandeja de entrada del cliente de una cuenta POP3, para identificar los mensajes que se han descargado o eliminado en ese cuenta.
    
## <a name="see-also"></a>Vea también

- [Administración de cuentas de Outlook](outlook-account-management.md)    
- [Localizar el historial de descarga de mensajes de una cuenta POP3](locating-the-message-download-history-for-a-pop3-account.md) 
- [Analizar el historial de descarga de mensajes de una cuenta POP3](parsing-the-message-download-history-for-a-pop3-account.md)   
- [PROP_POP_LEAVE_ON_SERVER](prop_pop_leave_on_server.md)  
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)    
- [Propiedades (API de administración de cuenta)](properties-account-management-api.md)
    

