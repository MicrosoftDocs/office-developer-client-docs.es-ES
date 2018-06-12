---
title: Obtener acceso a objetos mediante el uso de la sesión
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: ee20e73e5bc7bb6854b956da541d3a318a267d0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816394"
---
# <a name="accessing-objects-by-using-the-session"></a>Obtener acceso a objetos mediante el uso de la sesión

  
  
**Se aplica a**: Outlook 
  
El puntero de sesión que recibe de la llamada a [MAPILogonEx](mapilogonex.md) puede utilizarse para tener acceso a una amplia variedad de objetos. En la siguiente tabla se enumera los métodos que se usan para tener acceso a varios objetos: 
  
|**Object**|**Método de sesión**|
|:-----|:-----|
|Sección de perfil  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Almacén de mensajes  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Libreta de direcciones  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objeto de administración del servicio de mensajes  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Carpeta, mensaje, el contenedor de la libreta de direcciones, lista de distribución o usuario de mensajería  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Con el método **OpenEntry** y un identificador de entrada válido, puede abrir cualquier objeto dirección proveedor de almacén de libro o un mensaje. Hay otros métodos de **OpenEntry** en MAPI, además del método **IMAPISession** . **OpenEntry** se implementa en los objetos siguientes: 
  
|**Object**|**M?todo**|
|:-----|:-----|
|Objeto de inicio de sesión del proveedor de la libreta de direcciones  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Libreta de direcciones  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Contenedor de la libreta de direcciones  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Sesión  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Almacén de mensajes  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objeto de inicio de sesión del proveedor de almacén de mensajes  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Carpeta  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objeto de soporte técnico  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Algunos métodos de **OpenEntry** requieren un identificador de entrada del objeto que se va a abrir, al igual que **IMAPISession::OpenEntry**; otros métodos que permiten NULL que se especifique. Un identificador de entrada NULL se interpreta de forma diferente dependiendo del objeto. Por ejemplo, cuando se llama a **IAddrBook::OpenEntry** con un identificador de entrada NULL, MAPI abre el contenedor de raíz de la libreta de direcciones. Método de **OpenEntry** del almacén de mensajes se comporta de forma similar; se abre la carpeta raíz del almacén de mensajes. **IMAPIContainer::OpenEntry**, implementada por las carpetas y los contenedores de la libreta de direcciones, puede devolver MAPI_E_INVALID_PARAMETER o el contenedor raíz, dependiendo del implementador. 
  
Además de no permitir un valor NULL para el identificador de entrada, **OpenEntry** método la sesión difiere otros métodos **OpenEntry** debido a que su trabajo no es abrir objetos. En su lugar, se examina el identificador de entrada y reenvía la llamada a otro método **OpenEntry** implementada por el proveedor de servicios adecuado. Por ejemplo, si se llama a **IMAPISession::OpenEntry** con el identificador de entrada de un mensaje, MAPI llama al método **IMSLogon::OpenEntry** del almacén de mensajes responsable del mensaje. 
  
Además de usar la sesión para abrir los objetos, los clientes use para compararlos. El método [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) compara objetos mediante la comparación de sus identificadores de entrada. Si las estructuras [MAPIUID](mapiuid.md) dentro de los identificadores de entrada pertenecen al mismo proveedor de servicios, MAPI reenvía la llamada a ese proveedor. **CompareEntryIDs** devuelve un valor de error cuando no coinciden con los identificadores de dos entrada. Aunque este método puede comparar los identificadores de entrada que pertenecen a cualquier tipo de objeto, **CompareEntryIDs** funciona mejor para objetos de nivel superior, como los almacenes de mensajes y los contenedores de la libreta de direcciones. Para comparar los objetos de nivel inferiores, compare directamente las claves de búsqueda de los objetos (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) o claves de registro (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Al igual que **OpenEntry**, **CompareEntryIDs** se implementa mediante varios objetos. Elija qué método **OpenEntry** y **CompareEntryID** a usar según la cantidad de información que tiene sobre el objeto o los objetos que se abre o en comparación. Use las siguientes instrucciones al decidir qué método de interfaz para llamar a: 
  
- Si no tiene ninguna información acerca de los objetos de destino, llame a [IMAPISession::OpenEntry](imapisession-openentry.md) o [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Este enfoque permite el acceso a cualquier objeto, pero es la más lenta de las tres.
    
- Si sabe que los objetos de destino son entradas de la libreta de direcciones en lugar de, por ejemplo, las carpetas, llame al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) o [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) . **IAddrBook::OpenEntry** abre el contenedor de raíz de la libreta de direcciones cuando se especifica NULL como el objeto de destino. Este enfoque permite el acceso a cualquier objeto de la libreta de direcciones y es más rápido que utilizar **IMAPISession**, pero es más lento que utilizar **IMAPIContainer**.
    
- Si el identificador de entrada que se utiliza es un identificador de entrada a corto plazo o si sabe que los objetos de destino pertenecen a un contenedor de la libreta de direcciones concreto o una carpeta, llame al método [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) . Este enfoque proporciona el rendimiento más rápido, pero permite el acceso sólo a los objetos de un contenedor específico o una carpeta. 
    

