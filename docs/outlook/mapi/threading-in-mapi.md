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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344833"
---
# <a name="threading-in-mapi"></a>Subprocesos en MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un subproceso es la entidad básica a la que un sistema operativo asigna tiempo de CPU. Un subproceso tiene sus propios registros, pila, prioridad y almacenamiento, pero comparte un espacio de direcciones y procesa recursos como los tokens de acceso. Los subprocesos también comparten memoria, con un subproceso que Lee lo que otro subproceso ha escrito.
  
Los clientes MAPI usan los siguientes modelos de subprocesos genéricos.
  
|**Modelo de subProcesos**|**Descripción**|
|:-----|:-----|
|Modelo de subprocesamiento único  <br/> |Todos los objetos se usan en un único subproceso.  <br/> |
|Modelo de subprocesos de apartamentos  <br/> |Un objeto solo puede usarse en el subproceso que lo creó.  <br/> |
|Modelo de subprocesamiento libre, o entidad de subproceso  <br/> |Un objeto puede usarse en cualquier subproceso.  <br/> |
   
MAPI utiliza el modelo de subprocesamiento libre, es decir, admite objetos seguros para subprocesos que se pueden usar en cualquier subproceso en cualquier momento. OLE utiliza el modelo de subprocesos de apartamentos. El modelo de subprocesos de apartamentos admite objetos que deben transferirse explícitamente cuando un subproceso distinto del que creó el objeto necesita usar ese objeto.
  
El mecanismo que usa OLE para transferir objetos de un subproceso a otro se conoce como cálculo de referencias. El cálculo de referencias implica un objeto de código auxiliar y un objeto proxy. Estos objetos especiales empaquetan los parámetros de la interfaz en el objeto que se va a calcular, se transfieren estos parámetros al otro subproceso y se descargan al llegar. El conflicto entre los dos modelos multiproceso surge cuando se envía un objeto MAPI de subprocesamiento libre a otro proceso mediante la llamada de procedimiento remoto "ligero" de OLE o LRPC. LRPC cambia la semántica del objeto del subprocesamiento libre al subprocesamiento de Apartamento mediante interfaces de código auxiliar y proxy intercambiadas con el comportamiento de los subprocesos de apartamento entre el objeto y el autor de la llamada. El conocimiento de las situaciones de MAPI que conducen a este conflicto puede ayudar a los clientes y a los proveedores de servicios a evitar que se produzcan problemas.
  
Se puede tener acceso A un objeto MAPI:
  
- Mediante llamadas directas a sus métodos mediante un puntero de interfaz devuelto por un proveedor de servicios o MAPI vinculado al proceso del cliente, como el objeto Session devuelto desde [MAPILogonEx](mapilogonex.md).
    
- Mediante llamadas indirectas a sus métodos mediante un puntero de interfaz devuelto por un proveedor de servicios, como el objeto Folder copiado de otra carpeta en [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md).
    
- Mediante una función de devolución de llamada, como el método [IMAPIAdviseSink:: método Notify](imapiadvisesink-onnotify.md) que se pasa a un proveedor de servicios **** o a MAPI en una llamada a Advise o a los métodos que pueden mostrar el progreso en una operación prolongada. 
    

