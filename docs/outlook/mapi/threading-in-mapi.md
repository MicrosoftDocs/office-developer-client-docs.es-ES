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
ms.openlocfilehash: 15fb6113e9c3428cff3865307736592fd6e2b2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820859"
---
# <a name="threading-in-mapi"></a>Subprocesos en MAPI

  
  
**Hace referencia a**: Outlook 
  
Un subproceso es la entidad básica a la que el sistema operativo asigna tiempo de CPU. Un subproceso tiene su propio registros, la pila, la prioridad y el almacenamiento, pero comparte una dirección espacio y el proceso de los recursos, como los tokens de acceso. Los subprocesos comparten también memoria, con lo que haya escrito otro subproceso de lectura de un subproceso.
  
Los clientes MAPI usan los siguientes modelos de subprocesamiento genéricos.
  
|**Modelo de subprocesos**|**Descripción**|
|:-----|:-----|
|Modelo de subprocesamiento único  <br/> |Todos los objetos se usan en el único subproceso.  <br/> |
|Modelo de subprocesamiento controlado  <br/> |Un objeto puede usarse solo en el subproceso que lo creó.  <br/> |
|Modelo de subprocesamiento libre o subproceso de terceros  <br/> |Un objeto puede usarse en cualquier subproceso.  <br/> |
   
MAPI utiliza el modelo de subprocesamiento libre, compatibilidad con objetos de subprocesos que se pueden usar en cualquier subproceso en cualquier momento. OLE utiliza el modelo de subprocesamiento controlado. El modelo de subprocesos de apartamento es compatible con los objetos que se deben transferir explícitamente cuando un subproceso distinto del que creó el objeto necesita utilizar ese objeto.
  
El mecanismo que utiliza OLE para transferir los objetos de un subproceso a otro se conoce como cálculo de referencias. El cálculo de referencias implica un objeto de código auxiliar y un objeto proxy. Estos objetos especiales empaquetar los parámetros de la interfaz en el objeto se puede ordenar, transferir estos parámetros para el otro subproceso y desempaquetar ellos a su llegada. Conflicto entre los dos modelos de multiproceso se produce cuando se envía un objeto MAPI subprocesamiento libre a otro proceso con OLE "ligero" llamada a procedimiento remoto o LRPC. LRPC cambia semántica del objeto de subprocesamiento libre para subprocesamiento controlado por interpone interfaces de proxy y código auxiliar con comportamiento entre el objeto y su autor de la llamada de subprocesamiento controlado. Conocimiento de las situaciones en MAPI que conducen a este conflicto puede ayudar a los clientes y proveedores de servicios de impedir que se produzca problemas.
  
Puede tener acceso a un objeto MAPI:
  
- A través de llamadas directas a sus métodos mediante una interfaz de puntero devuelto por un proveedor de servicios o MAPI vinculadas al proceso del cliente, como el objeto de sesión devuelto desde [MAPILogonEx](mapilogonex.md).
    
- A través de llamadas indirectas a sus métodos con un puntero de interfaz devuelto por cualquier proveedor de servicios, como el objeto de carpeta copió desde otra carpeta en [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).
    
- A través de una función de devolución de llamada, como el método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pasada a un proveedor de servicios o a MAPI en una llamada **Advise** o los métodos que pueden mostrar el progreso de una operación prolongada. 
    

