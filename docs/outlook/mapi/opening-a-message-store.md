---
title: Abrir un almacén de mensajes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4bab31dbcd1f7139980d7df5559c1ee52a6f167f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563649"
---
# <a name="opening-a-message-store"></a>Abrir un almacén de mensajes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Dependiendo del perfil, un cliente tendrá que abrir uno o más almacenes de mensaje durante una sesión típica. Abrir un almacén de mensajes significa para obtener acceso a un puntero a su [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) implementación. La interfaz de **IMsgStore** proporciona los métodos de notificación, hacer que las asignaciones de carpetas y obtener acceso a carpetas y mensajes. 
  
Los clientes abren los almacenes de mensajes en el inicio de sesión y cuando se modifica un perfil. Si el cliente permite a los usuarios agregar almacenes de mensajes para el perfil durante una sesión activa, puede abrirlos inmediatamente u omitirlos hasta la siguiente sesión. Si se registra para recibir notificaciones en la tabla de almacenamiento de mensajes, se le avisará a la disponibilidad de un nuevo almacén de mensajes.
  
Para abrir un almacén de mensajes, debe tener su identificador de entrada disponible. La mayoría de los clientes tener acceso a los identificadores de entrada de los almacenes de mensajes que desean abrir a través de la tabla de almacén de mensajes. Sin embargo, algunos mensajes almacena el formato de sus identificadores de entrada, lo que permite a los clientes el desvío de la tabla de almacén de mensajes y construir el identificador de entrada necesario del documento. Este identificador de entrada puede pasar directamente a [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) y MAPI crea automáticamente una sección de perfil para el proveedor sin asociarla con cualquier servicio de mensajes. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Recuperar un identificador de entrada de la tabla de almacén de mensajes
  
1. Llame a [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para abrir la tabla de almacén de mensajes. 
    
2. Llame a **IMAPITable::SetColumns** para limitar la tabla a un conjunto de columna pequeña que incluye las siguientes columnas: 
    
   - **PR_PROVIDER_DISPLAY** o **PR_DISPLAY_NAME**
   - Propiedades de **entrada del objeto** 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Crear una restricción para filtrar la fila que representa el almacén de mensajes que se va a abrir. Para obtener más información acerca de buscando el almacén de mensajes de forma predeterminada, vea [Abrir el almacén de mensajes predeterminado](opening-the-default-message-store.md). Para buscar un almacén de mensajes por su nombre, aplicar cualquiera de las restricciones de propiedad siguientes:
    
   - Coincidencia de **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) con el nombre general para este tipo de almacén de mensajes. Por ejemplo, se puede establecer PR_PROVIDER_DISPLAY en "Carpetas personales".
    
   - Coincidencia **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) con la específica **MAPIUID** para este tipo de almacén de mensajes. 
    
   - Coincidencia **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre para este almacén de mensajes determinado. Por ejemplo, **PR_DISPLAY_NAME** puede estar establecido en "Mis mensajes para el año Fiscal 2010". 
    
4. Llame a [HrQueryAllRows](hrqueryallrows.md) para recuperar la fila correspondiente de la tabla de almacén de mensajes. El identificador de entrada de la fila se incluirá en la matriz de valores de propiedad para el miembro **aRow** del conjunto de filas que apunta el parámetro _pprows_ . 
    
5. Llame a [FreeProws](freeprows.md) para liberar el conjunto de filas que apunta _pprows_.
    
6. Versión en la tabla de almacenamiento de mensaje mediante una llamada a su método **IUnknown:: Release** . 
    
Si ha creado un identificador de entrada personalizado para el almacén de mensajes que se abrirá, llame a la función [WrapStoreEntryID](wrapstoreentryid.md) para convertir a un identificador de entrada estándar. 
  
Una vez que tenga el identificador de entrada de un almacén de mensajes, llame a uno de los métodos siguientes para abrirlo:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Llamar a **OpenMsgStore** si necesita especificar una amplia variedad de opciones especiales para el almacén de mensajes. **OpenMsgStore** le permite suprimir la visualización de cuadros de diálogo, identificar el almacén de mensajes como temporal o como un almacén nonmessaging, establecer niveles de acceso y para aplazar errores. **OpenEntry** , sólo puede establecer niveles de acceso y aplazar errores. 
  
Establecer el MDB_NO_MAIL marca indica a MAPI que no se utilizará el almacén de mensajes para enviar o recibir mensajes. MAPI no comunicar a la cola MAPI sobre la existencia de este almacén de mensajes. El indicador MDB_TEMPORARY designa un almacén de mensajes como temporal, lo que implica que no puede usarse para almacenar información permanente. Almacenes de mensaje temporal no aparecen en la tabla de almacén de mensajes. 
  
## <a name="see-also"></a>Recursos adicionales

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

