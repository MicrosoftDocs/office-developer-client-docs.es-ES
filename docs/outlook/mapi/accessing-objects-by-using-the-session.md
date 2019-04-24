---
title: Obtener acceso a objetos mediante la sesión
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a76397b74642aedf9ad5c9704735d869f61db7e3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321710"
---
# <a name="accessing-objects-by-using-the-session"></a>Obtener acceso a objetos mediante la sesión

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El puntero de sesión que recibe de la llamada a [MAPILogonEx](mapilogonex.md) puede usarse para obtener acceso a una amplia variedad de objetos. En la tabla siguiente se enumeran los métodos que se usan para tener acceso a varios objetos: 
  
|**Objeto**|**Método Session**|
|:-----|:-----|
|Sección de perfil  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Almacén de mensajes  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Libreta de direcciones  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objeto de administración del servicio de mensajes  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Carpeta, mensaje, contenedor de libreta de direcciones, lista de distribución o usuario de mensajería  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Con el método **OpenEntry** y un identificador de entrada válido, puede abrir cualquier objeto de la libreta de direcciones o del proveedor de almacenamiento de mensajes. Existen otros métodos **OpenEntry** en MAPI, además del método **IMAPISession** . **OpenEntry** se implementa en los objetos siguientes: 
  
|**Objeto**|**Método**|
|:-----|:-----|
|Objeto de inicio de sesión del proveedor de libreta de direcciones  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Libreta de direcciones  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Contenedor de libreta de direcciones  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Session  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Almacén de mensajes  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objeto de inicio de sesión del proveedor de almacenamiento de mensajes  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objeto support  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Algunos métodos **OpenEntry** requieren un identificador de entrada del objeto que se va a abrir, como hace **IMAPISession:: OpenEntry**; otros métodos permiten especificar NULL. Un identificador de entrada NULL se interpreta de manera diferente según el objeto. Por ejemplo, cuando se llama a **IAddrBook:: OpenEntry** con un identificador de entrada null, MAPI abre el contenedor raíz de la libreta de direcciones. El método **OpenEntry** del almacén de mensajes se comporta de manera similar; abre la carpeta raíz del almacén de mensajes. **IMAPIContainer:: OpenEntry**, implementado por carpetas y contenedores de libretas de direcciones, puede devolver MAPI_E_INVALID_PARAMETER o el contenedor raíz, según el implementador. 
  
Además de no permitir un valor NULL para el identificador de entrada, el método **OpenEntry** de la sesión difiere de otros métodos **OpenEntry** porque su trabajo no es abrir objetos. En su lugar, examina el identificador de la entrada y reenvía la llamada a otro método **OpenEntry** implementado por el proveedor de servicios correspondiente. Por ejemplo, si llama a **IMAPISession:: OpenEntry** con el identificador de entrada de un mensaje, MAPI llama al método **IMSLogon:: OpenEntry** del almacén de mensajes responsable del mensaje. 
  
Además de usar la sesión para abrir objetos, los clientes la usan para compararlas. El método [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) compara objetos comparando sus identificadores de entrada. Si las estructuras [MAPIUID](mapiuid.md) incluidas en los identificadores de entrada pertenecen al mismo proveedor de servicios, MAPI reenvía la llamada a ese proveedor. **CompareEntryIDs** devuelve un valor de error cuando los dos identificadores de entrada no coinciden. Aunque este método puede comparar los identificadores de entrada que pertenecen a cualquier tipo de objeto, **CompareEntryIDs** funciona mejor para objetos de nivel superior, como almacenes de mensajes y contenedores de libretas de direcciones. Para comparar objetos de nivel inferior, compare directamente las claves de búsqueda de los objetos (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) o las claves de registro (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Al igual que **OpenEntry**, **CompareEntryIDs** se implementa mediante varios objetos. Elija qué método **OpenEntry** y **CompareEntryID** usar de acuerdo con la cantidad de información que tiene sobre el objeto u objetos que se van a abrir o comparar. Siga estas directrices a la hora de decidir el método de interfaz al que llamar: 
  
- Si no tiene información sobre los objetos de destino, llame a [IMAPISession:: OpenEntry](imapisession-openentry.md) o [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md). Este enfoque permite el acceso a cualquier objeto, pero es el más lento de los tres.
    
- Si sabe que los objetos de destino son entradas de la libreta de direcciones en lugar de, por ejemplo, las carpetas, llame al método [IAddrBook:: OpenEntry](iaddrbook-openentry.md) o [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md) . **IAddrBook:: OpenEntry** abre el contenedor raíz de la libreta de direcciones cuando se especifica NULL como el objeto de destino. Este enfoque permite el acceso a cualquier objeto de la libreta de direcciones y es más rápido que el uso de **IMAPISession**, pero es más lento que el uso de **IMAPIContainer**.
    
- Si el identificador de entrada que se usa es un identificador de entrada a corto plazo o si sabe que los objetos de destino pertenecen a una carpeta o contenedor de libreta de direcciones en particular, llame al método [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) . Este enfoque produce el rendimiento más rápido, pero permite el acceso solo a los objetos de un contenedor o carpeta específicos. 
    

