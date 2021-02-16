---
title: Uso de Thread-Safe objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425172"
---
# <a name="using-thread-safe-objects"></a>Uso de Thread-Safe objetos

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Las aplicaciones cliente pueden suponer que los objetos usados directamente o como devoluciones de llamada siempre son seguros para subprocesos, excepto en los siguientes casos:
  
- Objeto de estado de un proveedor de transporte obtenido a través de una llamada de cliente a [IMAPISession::OpenEntry con](imapisession-openentry.md) un identificador de entrada de la fila de tabla de estado del proveedor. 
    
- Todos los objetos de formulario MAPI obtenidos a través de una llamada de cliente a [MAPIOpenFormMgr](mapiopenformmgr.md). Los objetos de formulario cumplen las reglas del modelo de departamentos y los clientes deben usarlos y todos los objetos contenidos en ellos solo en el subproceso que las creó.
    
Cuando un cliente tiene acceso a la fila de un proveedor de transporte en la tabla de estado que incluye el identificador de entrada del objeto de estado asociado, el cliente puede llamar a **OpenEntry** con ese identificador de entrada para abrir el objeto de estado. Este objeto de estado no es seguro para subprocesos porque los proveedores de transporte se ejecutan en el contexto de la cola MAPI y no mantienen un contexto independiente para su objeto de estado. El objeto de estado cumple las reglas del modelo de departamentos y los clientes solo deben usarlo en el subproceso que lo creó. 
  
Un cliente también debe invocar [MAPIInitialize](mapiinitialize.md) en cada subproceso antes de usar cualquier objeto MAPI y [MAPIUninitialize](mapiuninitialize.md) cuando se complete ese uso. Estas llamadas deben realizarse incluso si los objetos que se van a usar se pasan al subproceso desde un origen externo. Se puede llamar a **MAPIInitialize** y **MAPIUninitialize** desde cualquier lugar excepto desde dentro de una función **DllMain** de Win32, una función que invoca el sistema cuando se inicializan y finalizan procesos y subprocesos, o cuando se llaman a las funciones **LoadLibrary** y **FreeLibrary.** 
  
Nunca se debe suponer que los objetos de uso indirecto son seguros para subprocesos. Los métodos que requieren punteros de interfaz de destino como parámetros de entrada devuelven objetos de uso indirecto. Algunos ejemplos de estos métodos son **IMAPIProp::CopyTo** y **CopyProps**, **IMAPIFolder::CopyFolder** y **CopyMessage** e **IMsgServiceAdmin::CopyMsgService**. Si un proveedor de servicios desea llamar a un objeto de este tipo desde un subproceso distinto del que se pasó, el proveedor es responsable de calcular explícitamente las referencias del objeto.
  

