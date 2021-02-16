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
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412040"
---
# <a name="closeimsgsession"></a>CloseIMsgSession

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cierra una sesión de mensaje y todos los mensajes creados en esa sesión. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Imessage.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a>Parámetros

 _lpMsgSess_
  
> [entrada] Puntero al objeto de sesión de mensaje obtenido mediante la [función OpenIMsgSession](openimsgsession.md) al inicio de la sesión del mensaje. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente y los proveedores de servicios que desean tratar con varios objetos **MAPI IMessage** relacionados basados en objetos OLE **IStorage** subyacentes usan una sesión de mensaje. El cliente o el proveedor usa las funciones [OpenIMsgSession](openimsgsession.md) y **CloseIMsgSession** para encapsular la creación de estos mensajes dentro de una sesión de mensaje. Una vez abierta la sesión del mensaje, el cliente o el proveedor le pasa un puntero en una llamada a [OpenIMsgOnIStg](openimsgonistg.md) para crear un nuevo **objeto IMessage**-on- **IStorage.** 
  
Una sesión de mensaje realiza un seguimiento de todos los objetos **IMessage**-on- **IStorage** abiertos durante la sesión, además de todos los datos adjuntos y otras propiedades de los mensajes. Cuando un cliente o proveedor llama **a CloseIMsgSession,** cierra todos estos objetos. Llamar **a CloseIMsgSession** es la única forma de cerrar **objetos IMessage**-on- **IStorage.** 
  

