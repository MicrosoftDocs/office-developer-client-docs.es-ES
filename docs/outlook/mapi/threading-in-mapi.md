---
title: Subprocesos en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405544"
---
# <a name="threading-in-mapi"></a>Subprocesos en MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un subproceso es la entidad básica a la que un sistema operativo asigna tiempo de CPU. Un subproceso tiene sus propios registros, pila, prioridad y almacenamiento, pero comparte un espacio de direcciones y recursos de proceso como tokens de acceso. Los subprocesos también comparten memoria, con un subproceso que lee lo que otro subproceso ha escrito.
  
Los clientes MAPI usan los siguientes modelos de subprocesos genéricos.
  
|**Modelo de subprocesos**|**Descripción**|
|:-----|:-----|
|Modelo de subproceso único  <br/> |Todos los objetos se usan en el único subproceso.  <br/> |
|Modelo de subprocesos de departamentos  <br/> |Un objeto solo se puede usar en el subproceso que lo creó.  <br/> |
|Modelo de subprocesos gratuitos o de grupo de subprocesos  <br/> |Se puede usar un objeto en cualquier subproceso.  <br/> |
   
MAPI usa el modelo de subprocesos gratuitos, que admite objetos seguros para subprocesos que se pueden usar en cualquier subproceso en cualquier momento. OLE usa el modelo de subprocesos de apartamento. El modelo de subprocesos de departamentos admite objetos que deben transferirse explícitamente cuando un subproceso distinto del que creó el objeto necesita usar ese objeto.
  
El mecanismo que OLE usa para transferir objetos de un subproceso a otro se conoce como cálculo de referencias. El cálculo de referencias implica un objeto stub y un objeto proxy. Estos objetos especiales empaquetan los parámetros de la interfaz del objeto que se va a calcular, transfieren estos parámetros al otro subproceso y los desenvasan al llegar. El conflicto entre los dos modelos multiproceso se produce cuando se envía un objeto MAPI de subproceso libre a otro proceso mediante llamada a procedimiento remoto "ligera" OLE o LRPC. LRPC cambia la semántica del objeto de subprocesos libres a subprocesos de departamentos mediante la interposición de interfaces de código auxiliar y proxy con el comportamiento de subproceso de apartamento entre el objeto y su autor de la llamada. El conocimiento de las situaciones en MAPI que llevan a este conflicto puede ayudar a los clientes y proveedores de servicios a evitar que se produzcan problemas.
  
Se puede obtener acceso a un objeto MAPI:
  
- A través de llamadas directas a sus métodos mediante un puntero de interfaz devuelto por un proveedor de servicios o MAPI vinculado al proceso del cliente, como el objeto de sesión devuelto de [MAPILogonEx](mapilogonex.md).
    
- A través de llamadas indirectas a sus métodos mediante un puntero de interfaz devuelto por cualquier proveedor de servicios, como el objeto folder copiado de otra carpeta en [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).
    
- A través de una función de devolución de llamada, como el método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pasado a un proveedor de servicios o a MAPI en una llamada **Advise** o los métodos que pueden mostrar el progreso de una operación larga. 
    

