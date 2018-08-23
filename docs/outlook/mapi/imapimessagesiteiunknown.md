---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cffa3024b8533f07f8f76fa5bbac219e23d61bdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589507"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Manipula los mensajes y se implementa mediante el código de formulario Visor (normalmente, una aplicación de cliente) que responde a esa manipulación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Expuestos por:  <br/> |Objetos de sitio de mensaje  <br/> |
|Se implementa mediante:  <br/> |Visores de formulario  <br/> |
|Llamado por:  <br/> |Objetos de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIMessageSite  <br/> |
|Tipo de puntero:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Devuelve la sesión MAPI en el que se ha creado o abierto el mensaje actual.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Devuelve el almacén de mensajes que contiene el mensaje actual, si existe un almacén de este tipo.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Devuelve la carpeta en la que el mensaje actual se ha creado o abierto, si existe una carpeta de este tipo.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Devuelve el mensaje actual.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Devuelve una interfaz de administrador de formulario, que puede usar un servidor de formulario para abrir otro servidor de formulario.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Crea un nuevo mensaje.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Copia el mensaje actual en una carpeta.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Mueve el mensaje actual a una carpeta.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Elimina el mensaje actual.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Solicitudes que se guarde el mensaje actual.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Solicitudes que se ponen en cola en el mensaje actual para la entrega.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Devuelve información de un objeto de sitio de mensaje acerca del mensaje de las capacidades del sitio para el mensaje actual.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el que se producen en el objeto de sitio de mensaje de error anterior.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

