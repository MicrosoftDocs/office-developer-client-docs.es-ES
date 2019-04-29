---
title: Copiar o mover un mensaje o una carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413503"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>Copiar o mover un mensaje o una carpeta
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Un cliente puede usar uno de cuatro métodos para copiar o mover un mensaje o una carpeta:
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
Al establecer los indicadores y los parámetros apropiados **** , se puede realizar CopyTo y **CopyProps** para que funcione igual que **CopyFolder** o **CopyMessages**. Tenga en cuenta los siguientes aspectos a la hora de decidir qué método llamar:
  
- ¿Está copiando o moviendo una carpeta o un mensaje?
    
- ¿Cuánto sabe sobre la carpeta o el mensaje que se va a mover o copiar?
    
- ¿Cuántas de las propiedades de la carpeta o del mensaje se moverán o se copiarán?
    
Puede usar los métodos **IMAPIProp** para copiar o mover una carpeta o un mensaje. **IMAPIFolder:: CopyMessages** solo funciona con mensajes; **IMAPIFolder:: CopyFolder** solo funciona con carpetas. 
  
Mientras que el uso de los métodos **IMAPIFolder** no requiere ningún conocimiento de las propiedades que admite la carpeta o el mensaje que se va a copiar o mover, debe tener algunos conocimientos para usar los métodos **IMAPIProp** . Con **IMAPIProp:: CopyProps**, debe poder especificar explícitamente cuál de las propiedades de la carpeta o del mensaje desea copiar o mover. Con **IMAPIProp:: CopyTo**, a menos que desee copiar o mover todas las propiedades, debe especificar explícitamente cuáles se deben excluir. Para obtener más información acerca de estos métodos, consulte [copia de propiedades MAPI](copying-mapi-properties.md).
  
El número de propiedades que se va a copiar o mover puede afectar a la decisión sobre el método que se va a usar. Si va a copiar o mover varios mensajes, llame a **IMAPIFolder:: CopyMessages**. Una opción alternativa es llamar a **IMAPIProp:: CopyProps** para copiar solo la propiedad **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) de la carpeta. El siguiente procedimiento muestra cómo usar **CopyMessages**. 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>Para copiar o mover uno o más mensajes
  
1. Busque identificadores de entrada válidos para las carpetas de origen y de destino.
    
2. Para abrir estas carpetas en modo de lectura y escritura, llame a [IMAPISession:: OpenEntry](imapisession-openentry.md) o [IMsgStore:: OpenEntry](imsgstore-openentry.md) y establezca la marca MAPI_MODIFY. 
    
3. Compruebe que el puntero de interfaz devuelto desde **OpenEntry** es un puntero de interfaz **IMAPIFolder** . Si no es así, conviértala al tipo LPMAPIFOLDER. 
    
4. Cree una matriz de identificadores de entrada que representen uno o más mensajes que se van a copiar o mover. 
    
5. Llame a **IMAPIFolder:: CopyMessages** con los siguientes indicadores establecidos: 
    
   - MESSAGE_MOVE, si desea realizar una operación de movimiento. 
    
   - MESSAGE_DIALOG y pase un identificador de ventana en el parámetro _ulUIParam_ si desea que la carpeta muestre un indicador de progreso. 
    
6. Libere los punteros **IMAPIFolder** para las carpetas de origen y de destino. 
    
Si desea copiar el contenido completo de una carpeta a otra carpeta, llame al método **IMAPIFolder:: CopyFolder** o **IMAPIProp:: CopyTo** de la carpeta de origen. 
  
Para copiar algunas de las propiedades de una carpeta, llame a su método **IMAPIProp:: CopyProps** . Para copiar la mayoría de las propiedades de una carpeta, llame a **IMAPIProp:: CopyTo**. 
  
Por ejemplo, si quiere copiar las propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de una carpeta, tiene las siguientes opciones:
  
- Llame a **IMAPIFolder:: CopyFolder** para copiar todas las propiedades de la carpeta y, a continuación, elimine las no deseadas de la nueva carpeta. 
    
- Llame **** a CopyTo y excluya todas las propiedades de la carpeta excepto **PR_DISPLAY_NAME** y **PR_COMMENT**. 
    
- Llame a **CopyProps**, pasando **PR_DISPLAY_NAME** y **PR_COMMENT** en la matriz include. 
    
En este caso, **CopyProps** es la mejor opción porque está pensada para ser utilizada para copiar un pequeño conjunto de propiedades y es la llamada más fácil de implementar. 
  
Para copiar o mover sólo las propiedades de la carpeta, sin incluir los mensajes, llame al método **IMAPIProp:: CopyTo** de la carpeta y excluya las siguientes propiedades: 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
Los métodos Copy pueden devolver S_OK, que indican que el resultado es correcto, MAPI_W_PARTIAL_COMPLETION, que indica que se ha realizado parcialmente correctamente o un error. Si se devuelve MAPI_W_PARTIAL_COMPLETION, use la macro **HR_FAILED** para obtener acceso a un error más específico. Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).
  
Si copia mensajes de un almacén de mensajes en otro y Unicode no es compatible con ambas, tenga en cuenta que la información se puede perder debido a la conversión de la página de códigos. Por lo general, no se puede saber si los almacenes de mensajes admiten uno o ambos formatos, lo que impide determinar si se copian las propiedades de texto como cadenas ASCII o como cadenas Unicode. Si admite Unicode, intente realizar una copia Unicode; Si se produce un error con el valor de error MAPI_E_BAD_CHARWIDTH, se recurre a ASCII.
  

