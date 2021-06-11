---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326197"
---
# <a name="openimsgsession"></a>OpenIMsgSession

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Crea y abre una sesión de mensaje que agrupa los mensajes creados en ella. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Imessage.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a>Parameters

 _lpMalloc_
  
> [in] Puntero a un objeto de asignador de memoria que expone la [interfaz OLE IMalloc.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) MAPI debe usar este método de asignación al trabajar con la interfaz OLE [IStorage.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) 
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero. 
    
 _lppMsgSess_
  
> [salida] Puntero a un puntero al objeto de sesión de mensaje devuelto.
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Se abrió la sesión.
    
MAPI_E_INVALID_PARAMETER
  
>  _lpMalloc_ o  _lppMsgSess_ es NULL. 
    
MAPI_E_INVALID_FLAGS
  
> Se pasaron marcas no válidas.
    
MAPI_UNICODE
  
> Al llamar a esta función, un cliente o proveedor de servicios establece la marca MAPI_UNICODE para crear archivos .msg Unicode. El archivo [Imessage](imessageimapiprop.md) resultante muestra STORE_UNICODE_OK en su PR_STORE_SUPPORT_MASK y admite propiedades Unicode. 
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente y los proveedores de servicios usan una sesión de mensajes que desean tratar varios objetos IMessage de MAPI [relacionados: IMAPIProp](imessageimapiprop.md) creados sobre objetos OLE **IStorage** subyacentes. El cliente o el proveedor usa las **funciones OpenIMsgSession** y [CloseIMsgSession](closeimsgsession.md) para encapsular la creación de dichos mensajes dentro de una sesión de mensaje. Una vez abierta la sesión del mensaje, el cliente o el proveedor le pasa un puntero en una llamada a [OpenIMsgOnIStg](openimsgonistg.md) para crear un nuevo **objeto IMessage**-on- **IStorage.** 
  
Una sesión de mensaje realiza un seguimiento de todos los objetos **IMessage**-on- **IStorage** creados durante la duración de la sesión, además de todos los datos adjuntos y otras propiedades de los mensajes. Cuando un cliente o proveedor llama **a CloseIMsgSession**, cierra todos estos objetos. Llamar **a CloseIMsgSession** es la única forma de cerrar **objetos IMessage**-on- **IStorage.** 
  
 Los clientes y proveedores usan **OpenIMsgSession** para controlar varios mensajes relacionados como objetos OLE **IStorage.** Si solo se va a abrir uno de estos mensajes a la vez, no es necesario realizar un seguimiento de varios mensajes ni motivo para crear una sesión de mensaje con **OpenIMsgSession**. 
  
Dado que se trata de un objeto OLE subyacente, MAPI debe usar la asignación de memoria OLE. Para obtener más información acerca de los objetos de almacenamiento estructurado OLE y la asignación de memoria OLE, vea [OLE y Transferencia de datos](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx). 
  

