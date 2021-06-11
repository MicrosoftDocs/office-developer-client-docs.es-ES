---
title: Acceso a objetos mediante el uso de la sesión
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a76397b74642aedf9ad5c9704735d869f61db7e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410542"
---
# <a name="accessing-objects-by-using-the-session"></a>Acceso a objetos mediante el uso de la sesión

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El puntero de sesión que recibe de la llamada a [MAPILogonEx](mapilogonex.md) se puede usar para obtener acceso a una amplia variedad de objetos. En la tabla siguiente se enumeran los métodos que se usan para obtener acceso a varios objetos: 
  
|**Objeto**|**Método Session**|
|:-----|:-----|
|Sección Perfil  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Almacén de mensajes  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Libreta de direcciones  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objeto de administración del servicio de mensajes  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Carpeta, mensaje, contenedor de libreta de direcciones, lista de distribución o usuario de mensajería  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Con el **método OpenEntry** y un identificador de entrada válido, puede abrir cualquier objeto de proveedor de libreta de direcciones o almacén de mensajes. Hay otros **métodos OpenEntry** en MAPI, además del **método IMAPISession.** **OpenEntry** se implementa en los siguientes objetos: 
  
|**Objeto**|**Método**|
|:-----|:-----|
|Objeto de inicio de sesión del proveedor de libreta de direcciones  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Libreta de direcciones  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Contenedor de libreta de direcciones  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Sesión  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Almacén de mensajes  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objeto de inicio de sesión del proveedor del almacén de mensajes  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Carpeta  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objeto Support  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Algunos **métodos OpenEntry** requieren un identificador de entrada del objeto que se va a abrir, al igual que **IMAPISession::OpenEntry**; otros métodos permiten que se especifique NULL. Un identificador de entrada NULL se interpreta de forma diferente en función del objeto. Por ejemplo, cuando se llama a **IAddrBook::OpenEntry** con un identificador de entrada NULL, MAPI abre el contenedor raíz de la libreta de direcciones. El método **OpenEntry** del almacén de mensajes se comporta de forma similar; abre la carpeta raíz del almacén de mensajes. **IMAPIContainer::OpenEntry**, implementado por carpetas y contenedores de libreta de direcciones, puede devolver MAPI_E_INVALID_PARAMETER o el contenedor raíz, según el implementador. 
  
Además de permitir un valor NULL para el identificador de entrada, el método **OpenEntry** de la sesión difiere de otros métodos **OpenEntry** porque su trabajo no es abrir objetos. En su lugar, examina el identificador de entrada y reenvía la llamada a otro método **OpenEntry** implementado por el proveedor de servicios adecuado. Por ejemplo, si llama a **IMAPISession::OpenEntry con** el identificador de entrada de un mensaje, MAPI llama al método **IMSLogon::OpenEntry** del almacén de mensajes responsable del mensaje. 
  
Además de usar la sesión para abrir objetos, los clientes la usan para compararlos. El [método IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) compara objetos comparando sus identificadores de entrada. Si las [estructuras MAPIUID](mapiuid.md) contenidas en los identificadores de entrada pertenecen al mismo proveedor de servicios, MAPI reenvía la llamada a ese proveedor. **CompareEntryIDs** devuelve un valor de error cuando los dos identificadores de entrada no coinciden. Aunque este método puede comparar los identificadores de entrada que pertenecen a cualquier tipo de objeto, **CompareEntryIDs** funciona mejor para objetos de nivel superior, como almacenes de mensajes y contenedores de libreta de direcciones. Para comparar objetos de nivel inferior, compare directamente las claves de búsqueda de los objetos (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) o las claves de registro (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Al **igual que OpenEntry,** **CompareEntryIDs** se implementa mediante varios objetos. Elija el **método OpenEntry** y **CompareEntryID** que se va a usar según la cantidad de información que tenga sobre el objeto u objetos que se abrirán o compararán. Use las siguientes directrices al decidir qué método de interfaz llamar: 
  
- Si no tiene información sobre los objetos de destino, llame a [IMAPISession::OpenEntry](imapisession-openentry.md) o [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Este enfoque permite el acceso a cualquier objeto, pero es el más lento de los tres.
    
- Si sabe que los objetos de destino son entradas de libreta de direcciones en lugar de, por ejemplo, carpetas, llame al método [IAddrBook::OpenEntry](iaddrbook-openentry.md) o [IAddrBook::CompareEntryIDs.](iaddrbook-compareentryids.md) **IAddrBook::OpenEntry** abre el contenedor raíz de la libreta de direcciones cuando se especifica NULL como objeto de destino. Este enfoque permite el acceso a cualquier objeto de libreta de direcciones y es más rápido que **usar IMAPISession**, pero más lento que **usar IMAPIContainer**.
    
- Si el identificador de entrada que se usa es un identificador de entrada a corto plazo o si sabe que los objetos de destino pertenecen a un contenedor o carpeta de libreta de direcciones en particular, llame al método [IMAPIContainer::OpenEntry.](imapicontainer-openentry.md) Este enfoque proporciona el rendimiento más rápido, pero solo permite el acceso a objetos de un contenedor o carpeta específico. 
    

