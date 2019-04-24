---
title: Uso de objetos seguros para subProcesos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329592"
---
# <a name="using-thread-safe-objects"></a>Uso de objetos seguros para subProcesos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente pueden suponer que los objetos que se utilizan directamente o como devoluciones de llamada son siempre seguros para subprocesos excepto en los casos siguientes:
  
- Un objeto de estado de proveedor de transporte obtenido a través de una llamada de cliente a [IMAPISession:: OpenEntry](imapisession-openentry.md) con un identificador de entrada de la fila de la tabla de estado del proveedor. 
    
- Todos los objetos de formulario MAPI obtenidos a través de una llamada de cliente a [MAPIOpenFormMgr](mapiopenformmgr.md). Los objetos de formulario obedecen las reglas y los clientes del modelo de Apartamento deben usarlos y todos los objetos que contienen solo en el subproceso que los creó.
    
Cuando un cliente obtiene acceso a la fila de un proveedor de transporte en la tabla de estado que incluye el identificador de entrada del objeto de estado asociado, el cliente puede llamar a **OpenEntry** con ese identificador de entrada para abrir el objeto de estado. Este objeto de estado no es seguro para subprocesos porque los proveedores de transporte se ejecutan en el contexto de la cola MAPI y no mantienen un contexto independiente para su objeto de estado. El objeto de Estado obedece a reglas de modelo de apartamento y los clientes solo deben usarlo en el subproceso que la creó. 
  
Un cliente también debe invocar [MAPIInitialize](mapiinitialize.md) en cada subproceso antes de usar objetos MAPI y [MAPIUninitialize](mapiuninitialize.md) cuando se complete ese uso. Estas llamadas deben realizarse incluso si los objetos que se van a usar se pasan al subproceso desde un origen externo. Se puede llamar a **MAPIInitialize** y **MAPIUninitialize** desde cualquier lugar excepto desde dentro de una función **DllMain** de Win32, una función invocada por el sistema cuando se inicializan y finalizan procesos y subprocesos, o cuando se realiza una llamada al ** Funciones LoadLibrary** y **FreeLibrary** . 
  
Nunca se debe asumir que los objetos de uso inDirecto son seguros para subprocesos. Los métodos que requieren punteros de interfaz de destino como parámetros de entrada devuelven los objetos de uso inDirecto. Ejemplos de estos métodos son **IMAPIProp:: CopyTo** y **CopyProps**, **IMAPIFolder:: CopyFolder** y **CopyMessage**y IMsgServiceAdmin **:: CopyMsgService**. Si un proveedor de servicios desea llamar a un objeto de este tipo desde un subproceso distinto al en el que se pasó, el proveedor es responsable de calcular de forma explícita el objeto.
  

