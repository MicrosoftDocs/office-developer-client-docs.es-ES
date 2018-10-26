---
title: Almacenes de mensaje de s�lo lectura
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 752ff2d6-ca64-4507-adf1-4c054c321203
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: e0a66443194a3f89b47218ed9dc0ed9ad9c2df83
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584516"
---
# <a name="read-only-message-stores"></a>Almacenes de mensaje de s�lo lectura

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Un almac�n de mensajes de solo lectura es uno en la que ni el cliente MAPI ni la cola MAPI puede crear, modificar o eliminar los objetos en el almac�n de mensajes. Hay muchas razones de por qu� es posible que desee implementar un almac�n de mensajes de s�lo lectura. Por ejemplo, una empresa informes de cr�dito podr�a utilizar un almac�n de s�lo lectura para permitir que sus clientes o empleados ver, pero no cambiar informes de cr�dito individual. Si se elige crear un mensaje de s�lo lectura almacenar tiene implicaciones para la estructura del proveedor de almacenamiento y para el propio almac�n. Por ejemplo, un almac�n de mensajes de solo lectura no puede tener una carpeta Bandeja de salida, ya que, a continuaci�n, los clientes MAPI debe solicitar la creaci�n de nuevos mensajes salientes en esa carpeta. De forma similar, es responsabilidad del proveedor de almacenamiento para garantizar la integridad del mecanismo de almacenamiento subyacente.
  
Hay tres marcadores que se pueden establecer en la propiedad de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) del almacén de mensajes que admiten distintos niveles de acceso de solo lectura. The STORE_READONLY flag indicates that all [IMAPIProp: IUnknown](imapipropiunknown.md) interfaces on objects in the message store are read-only. The STORE_MODIFY_OK flag indicates that existing messages in the message store may be modified, but new folders and messages may not be created. The STORE_CREATE_OK flag indicates that new messages and folders may be created, but indicates nothing about whether existing objects may be modified. 
  
El hecho de que los clientes MAPI y la cola MAPI no sea capaz de crear, modificar o eliminar los objetos en el almac�n de mensajes no significa que no cambie nunca el contenido del mecanismo de almacenamiento subyacente. Ni significa que el proveedor de almac�n nunca necesita permiso de escritura para el mecanismo de almacenamiento subyacente. En algunas circunstancias esas dos condiciones pueden aplicar, pero no en el caso de un mensaje de s�lo lectura general almac�n. El nivel de acceso que requiere su proveedor de almacenamiento y si su proveedor de almacenamiento cambia alguna vez datos en el mecanismo de almacenamiento subyacente depende principalmente de la naturaleza espec�fica de su proveedor de almacenamiento.
  
Por ejemplo, si est� escribiendo un proveedor de almacenamiento para dar a los clientes MAPI acceso a una base de datos almacenada en un dispositivo de CD-ROM, no se puede cambiar el mecanismo de almacenamiento subyacente y su proveedor de almacenamiento puede tener el permiso de solo lectura. Si, sin embargo, est� escribiendo un proveedor de almacenamiento para conceder acceso de solo lectura de los clientes MAPI a una base de datos de carpetas p�blicas, pero el proveedor de almacenamiento que se necesita para realizar un seguimiento del estado le�do o de los mensajes de cada usuario, el proveedor de almacenamiento tendr� que escribir nuevos datos en el mecanismo de almacenamiento subyacente. Sin embargo, en ning�n ejemplo es el proveedor de almacenamiento nunca necesario que crear, modificar o eliminar las carpetas o mensajes a petici�n de los clientes MAPI o de la cola MAPI.
  
La lista corta de motivos por los que un proveedor de almac�n ser�a necesario para escribir datos en un mecanismo de almacenamiento subyacente en caso contrario, es de s�lo lectura es el siguiente:
  
- Para almacenar el estado le�do o de los mensajes.
    
- Para implementar notificaciones de lectura/nonread. 
    
- Para almacenar las vistas.
    
- Para almacenar en cach� los �ndices persistentes para criterios de ordenaci�n de la carpeta definida por el usuario.
    
- To store the sort order of a folder's contents (supporting [IMAPIFolder::SaveContentsSort](imapifolder-savecontentssort.md)).
    
- To store search criteria, search state, and results, if the message store provider supports searches (supporting [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)).
    
Si el proveedor de almac�n de mensajes nunca puede escribir datos en el mecanismo de almacenamiento subyacente, necesitar� implementar estas caracter�sticas mediante el uso de un mecanismo de almacenamiento independientes fuera el mecanismo de almacenamiento subyacente. Por ejemplo, un proveedor de almac�n de mensajes de s�lo lectura puede almacenar el estado le�do o de los mensajes en el almac�n en un archivo en el equipo del usuario. Esta estrategia presenta dificultades adicionales, pero puede ser los proveedores de almac�n para implementar algunas de las caracter�sticas de la manera de sea factible s�lo para el mensaje de s�lo lectura. Por ejemplo, mantener el contenido del mecanismo de almacenamiento independientes sincronizado con los objetos en el almac�n de mensajes es m�s dif�cil que almacenar el estado le�do o directamente en el propio almac�n de mensajes.
  
B�squeda presenta una complejidad adicional para los proveedores de almac�n de mensaje de s�lo lectura. Los clientes de usar la carpeta especificada en la propiedad de **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)) del objeto de almacén de mensajes para buscar la carpeta que se usa para los resultados de búsqueda. A menudo, los proveedores de almac�n de mensaje de s�lo lectura no pueden instalar una carpeta permanente de resultados de la b�squeda en el almac�n de mensajes. En ese caso, el proveedor de almacenamiento de mensajes debe almacenar un identificador de entrada en la propiedad **PR_FINDER_ENTRYID** que puede reconocer cuando los clientes abren carpetas para que puede crear din�micamente una carpeta de resultados de b�squeda en lugar de leer uno desde el mecanismo de almacenamiento subyacente. Sin embargo, muchos de los proveedores de almac�n de mensaje de s�lo lectura crean din�micamente todas sus carpetas, no es porque normalmente un exceso de una carga. 
  
El hecho de que el proveedor de almac�n de mensajes es de s�lo lectura se anuncia en propiedad de **PR_STORE_SUPPORT_MASK** del objeto de proveedor de almac�n. Sin embargo, no se cuentan en los clientes que respete esa propiedad; c�digo del proveedor de almacenamiento debe aplicar el estado de s�lo lectura del mecanismo de almacenamiento subyacente. 
  
## <a name="see-also"></a>Vea también



[Desarrollar un proveedor de almacén de mensajes MAPI](developing-a-mapi-message-store-provider.md)

