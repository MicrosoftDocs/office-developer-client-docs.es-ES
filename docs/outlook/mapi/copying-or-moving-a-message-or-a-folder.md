---
title: Copiar o mover un mensaje o una carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 26fe135da93e0f5f94d9f7d264453b74f97a518b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816610"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Copiar o mover un mensaje o una carpeta
  
**Se aplica a**: Outlook 
  
Un cliente puede usar uno de los cuatro métodos para copiar o mover un mensaje o una carpeta:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Mediante la configuración de los parámetros y los marcadores adecuados, **CopyTo** y **CopyProps** se pueden establecer para que funcione como **CopyFolder** o **CopyMessages**. Tenga en cuenta lo siguiente al decidir qué método de llamada:
  
- ¿Copiar o mover una carpeta o un mensaje?
    
- ¿Cuánto sabe acerca de la carpeta o el mensaje que se va a mover o copiar?
    
- ¿Cuántos de la carpeta o propiedades del mensaje que se va a mover o copiar?
    
Puede usar los métodos **IMAPIProp** para copiar o mover una carpeta o un mensaje. **IMAPIFolder::CopyMessages** funciona con los mensajes solamente; **IMAPIFolder::CopyFolder** funciona con carpetas sólo. 
  
Mientras que con los métodos **IMAPIFolder** no requieren ningún conocimiento de las propiedades compatibles con el mensaje para ser copiado o movido o la carpeta, debe tener conocimientos para usar los métodos **IMAPIProp** . Con **IMAPIProp::CopyProps**, debe especificar cuál de las propiedades de carpeta o mensaje que desee copiar o mover de forma explícita. Con **IMAPIProp::CopyTo**, a menos que desee copiar o mover todas las propiedades, se debe especificar explícitamente las que se deben excluir. Para obtener más información acerca de estos métodos, vea [Copiar las propiedades de MAPI](copying-mapi-properties.md).
  
El número de propiedades que se pueden copiar o mover puede afectar a su decisión sobre qué método va a usar. Si está copiando o moviendo varios mensajes, llame a **IMAPIFolder::CopyMessages**. Una opción alternativa es llamar a **IMAPIProp::CopyProps** para copiar sólo la propiedad de la carpeta **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). El procedimiento siguiente muestra cómo usar **CopyMessages**. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Para copiar o mover uno o más mensajes
  
1. Busque los identificadores de entrada válido para las carpetas de origen y de destino.
    
2. Abra estas carpetas en el modo de lectura y escritura mediante una llamada a [IMAPISession::OpenEntry](imapisession-openentry.md) o [IMsgStore::OpenEntry](imsgstore-openentry.md) y establecer el indicador MAPI_MODIFY. 
    
3. Compruebe que el puntero de interfaz devuelto desde **OpenEntry** es un puntero de interfaz **IMAPIFolder** . Si no es así, se convierte en el tipo LPMAPIFOLDER. 
    
4. Crear una matriz de identificadores de entrada que representa los mensajes de uno o más para ser copiado o movido. 
    
5. Llame al método **IMAPIFolder::CopyMessages** con el siguiente conjunto de indicadores: 
    
   - MESSAGE_MOVE, si desea realizar una operación de movimiento. 
    
   - Controlan MESSAGE_DIALOG y pase una ventana en el parámetro _ulUIParam_ , si desea que la carpeta que se va a mostrar un indicador de progreso. 
    
6. Liberar los punteros **IMAPIFolder** para las carpetas de origen y de destino. 
    
Si desea copiar el contenido completo de una carpeta a otra carpeta, llame al método de **IMAPIFolder::CopyFolder** o **IMAPIProp::CopyTo** de la carpeta de origen. 
  
Para copiar algunas de las propiedades de una carpeta, llame al método **IMAPIProp::CopyProps** . Para copiar la mayoría de las propiedades de una carpeta, llamar a **IMAPIProp::CopyTo**. 
  
Por ejemplo, si desea copiar una carpeta **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y las propiedades **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)), tiene las siguientes opciones:
  
- Llame a **IMAPIFolder::CopyFolder** para copiar todas las propiedades de carpeta y, a continuación, elimine los no deseados de la nueva carpeta. 
    
- Llame a **CopyTo** y todos los de las propiedades de la carpeta excepto **PR_DISPLAY_NAME** y **PR_COMMENT**excluir. 
    
- Llamar a **CopyProps**, pasando la matriz de incluir **PR_DISPLAY_NAME** y **PR_COMMENT** . 
    
En este caso, **CopyProps** es la mejor opción porque está diseñada para usarse para copiar un pequeño conjunto de propiedades y es la llamada más fácil implementar. 
  
Para copiar o mover sólo las propiedades de la carpeta, sin incluir los mensajes, llame al método **IMAPIProp::CopyTo** de la carpeta y excluir las siguientes propiedades: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Los métodos de copia pueden devolver S_OK, que indica éxito total, MAPI_W_PARTIAL_COMPLETION, que indica éxito parcial o un error. Si se devuelve MAPI_W_PARTIAL_COMPLETION, utilice la macro **HR_FAILED** para tener acceso a un error más específico. Para obtener más información, vea [Uso de Macros para el control de errores](using-macros-for-error-handling.md).
  
Si copiar mensajes desde el almacén de mensajes de uno a otro y Unicode no es compatible con ambos, tenga en cuenta que la información se puede perder debido a la conversión de página de código. Normalmente no se puede saber si los almacenes de mensajes admiten formatos de uno o ambos, que no se pueda determinar si se deben copiar las propiedades de texto como cadenas ASCII o como cadenas Unicode. Si admite Unicode, intenta realizar una copia de Unicode; Si se produce un error con el valor de error MAPI_E_BAD_CHARWIDTH, recurrir a ASCII.
  

