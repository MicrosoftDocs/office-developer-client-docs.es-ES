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
ms.openlocfilehash: 665c14b285db166e4f2a421d46e57f23e2f7ad52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432376"
---
# <a name="opening-a-message-store"></a>Abrir un almacén de mensajes

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Según el perfil, un cliente tendrá que abrir uno o varios almacenes de mensajes durante una sesión típica. Abrir un almacén de mensajes significa obtener acceso a un puntero a su [implementación IMsgStore : IMAPIProp.](imsgstoreimapiprop.md) La **interfaz IMsgStore** proporciona métodos para la notificación, la realización de asignaciones de carpetas y el acceso a carpetas y mensajes. 
  
Los clientes abren almacenes de mensajes al iniciar sesión y cuando se modifica un perfil. Si el cliente permite a los usuarios agregar almacenes de mensajes al perfil durante una sesión activa, puede abrirlos inmediatamente o ignorarlos hasta la siguiente sesión. Al registrarse para recibir notificaciones en la tabla de almacén de mensajes, se te avisará de la disponibilidad de un nuevo almacén de mensajes.
  
Para abrir un almacén de mensajes, debe tener su identificador de entrada disponible. La mayoría de los clientes tienen acceso a los identificadores de entrada de los almacenes de mensajes que desean abrir a través de la tabla de almacén de mensajes. Sin embargo, algunos almacenes de mensajes documentan el formato de sus identificadores de entrada, lo que permite a los clientes omitir la tabla de almacén de mensajes y crear el identificador de entrada necesario. Pueden pasar este identificador de entrada directamente a [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) y MAPI crea automáticamente una sección de perfil para el proveedor sin asociarlo con ningún servicio de mensajes. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Recuperar un identificador de entrada de la tabla de almacén de mensajes
  
1. Llame [a IMAPISession::GetMsgStoresTable para](imapisession-getmsgstorestable.md) abrir la tabla de almacén de mensajes. 
    
2. Llame **a IMAPITable::SetColumns** para limitar la tabla a un conjunto de columnas pequeño que incluya las siguientes columnas: 
    
   - **PR_PROVIDER_DISPLAY** o **PR_DISPLAY_NAME**
   - **PR_ENTRYID** propiedades 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Cree una restricción para filtrar la fila que representa el almacén de mensajes que se va a abrir. Para obtener más información acerca de cómo buscar el almacén de mensajes predeterminado, consulte [Opening the Default Message Store](opening-the-default-message-store.md). Para buscar un almacén de mensajes por su nombre, aplique cualquiera de las siguientes restricciones de propiedad:
    
   - Coincide **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) con el nombre general para este tipo de almacén de mensajes. Por ejemplo, PR_PROVIDER_DISPLAY se puede establecer en "Carpetas personales".
    
   - Coincide **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) con el **MAPIUID** específico para este tipo de almacén de mensajes. 
    
   - Coincide **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) con el nombre de este almacén de mensajes en particular. Por ejemplo, **PR_DISPLAY_NAME** puede establecerse en "Mis mensajes para el año fiscal 2010". 
    
4. Llame [a HrQueryAllRows](hrqueryallrows.md) para recuperar la fila adecuada de la tabla de almacén de mensajes. El identificador de entrada de la fila se incluirá en la matriz de valores de propiedad para el miembro **aRow** del conjunto de filas señalado por el _parámetro pprows._ 
    
5. Llama [a FreeProws](freeprows.md) para liberar el conjunto de filas señalado por  _pprows_.
    
6. Libere la tabla de almacén de mensajes llamando a su **método IUnknown::Release.** 
    
Si ha creado un identificador de entrada personalizado para que se abra el almacén de mensajes, llame a la [función WrapStoreEntryID](wrapstoreentryid.md) para convertirlo en un identificador de entrada estándar. 
  
Una vez que tenga el identificador de entrada de un almacén de mensajes, llame a uno de los siguientes métodos para abrirlo:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Llama **a OpenMsgStore** si necesitas especificar una variedad de opciones especiales para el almacén de mensajes. **OpenMsgStore** permite suprimir la presentación de cuadros de diálogo, identificar el almacén de mensajes como temporal o como un almacén que no está en uso, establecer niveles de acceso y aplazar errores. **OpenEntry** solo permite establecer niveles de acceso y aplazar errores. 
  
Al establecer la MDB_NO_MAIL indica a MAPI que el almacén de mensajes no se usará para enviar o recibir mensajes. MAPI no informa a la cola MAPI sobre la existencia de este almacén de mensajes. La MDB_TEMPORARY marca designa un almacén de mensajes como temporal, lo que implica que no se puede usar para almacenar información permanente. Los almacenes de mensajes temporales no aparecen en la tabla de almacén de mensajes. 
  
## <a name="see-also"></a>Vea también

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

