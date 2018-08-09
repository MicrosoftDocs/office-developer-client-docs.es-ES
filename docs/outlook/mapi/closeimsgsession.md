---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c190691c8cfcb9b049bcf9ee4f21436e20955def
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816544"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**Hace referencia a**: Outlook 
  
Cierra una sesión de mensajería y todos los mensajes creados dentro de esa sesión. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |IMessage.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Parámetros

 _lpMsgSess_
  
> [entrada] Puntero para el objeto de sesión de mensaje obtenido mediante la función [OpenIMsgSession](openimsgsession.md) al principio de la sesión de mensajería. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Una sesión de mensajería se usa en las aplicaciones cliente y proveedores de servicios que desean para abordar los problemas con varios objetos MAPI **IMessage** relacionados fundamentan objetos OLE **IStorage** subyacentes. El cliente o el proveedor utiliza las funciones [OpenIMsgSession](openimsgsession.md) y **CloseIMsgSession** para ajustar la creación de este tipo de mensajes dentro de una sesión de mensajería. Una vez que se abre la sesión de mensajería, el cliente o el proveedor pasa un puntero a ella en una llamada a [OpenIMsgOnIStg](openimsgonistg.md) para crear un nuevo **IMessage**- en - objeto **IStorage** . 
  
Una sesión de mensajería realiza un seguimiento de todos los objetos de **IMessage**- en - **IStorage** abiertos durante la duración de la sesión, además de todos los datos adjuntos y otras propiedades de los mensajes. Cuando un cliente o un proveedor de llamadas **CloseIMsgSession**, cierra todos estos objetos. Al llamar a **CloseIMsgSession** es la única forma de cerrar **IMessage**- en - objetos **IStorage** . 
  

