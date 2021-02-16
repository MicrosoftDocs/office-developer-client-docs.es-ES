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
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433370"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Manipula los mensajes y lo implementa el código del visor de formularios (normalmente una aplicación cliente) que responde a dicha manipulación.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiform.h  <br/> |
|Expuesto por:  <br/> |Objetos de sitio de mensajes  <br/> |
|Implementado por:  <br/> |Visores de formularios  <br/> |
|Llamado por:  <br/> |Objetos de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIMessageSite  <br/> |
|Tipo de puntero:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Devuelve la sesión MAPI en la que se creó o abrió el mensaje actual.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Devuelve el almacén de mensajes que contiene el mensaje actual, si existe dicho almacén.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Devuelve la carpeta en la que se creó o abrió el mensaje actual, si existe dicha carpeta.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Devuelve el mensaje actual.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Devuelve una interfaz de administrador de formularios, que un servidor de formulario puede usar para abrir otro servidor de formularios.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Crea un mensaje nuevo.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Copia el mensaje actual en una carpeta.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Mueve el mensaje actual a una carpeta.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Elimina el mensaje actual.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Solicita que se guarde el mensaje actual.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Solicita que el mensaje actual se pone en cola para su entrega.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Devuelve información de un objeto de sitio de mensaje acerca de las capacidades del sitio del mensaje para el mensaje actual.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se ha producido en el objeto de sitio del mensaje.  <br/> |
   
## <a name="see-also"></a>Consulte también



[Interfaces MAPI](mapi-interfaces.md)

