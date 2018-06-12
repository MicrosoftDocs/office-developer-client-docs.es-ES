---
title: Estado de NoScribble
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 41f5acddf273de39a7d5952ccb00e868170c692d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818423"
---
# <a name="noscribble-state"></a>Estado de NoScribble

  
  
**Se aplica a**: Outlook 
  
El estado de NoScribble indica que se están guardando los cambios realizados en un mensaje. El almacenamiento de valores almacenados en la interfaz de usuario del objeto de formulario real se produce cuando el formulario método del objeto [IPersistMessage::Save](ipersistmessage-save.md) se llama a la aplicación cliente. La siguiente tabla describe las transiciones permitidas desde el estado NoScribble. 
  
|IPersistMessage ** (método) **|**Acción**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage ==_ nulo)  <br/> |Si marca _fSameAsLoad_ era TRUE en la llamada [IPersistMessage::Save](ipersistmessage-save.md) que ha provocado el formulario para escribir el estado de NoScribble y el mensaje se ha modificado, internamente marcar los cambios como si estuviera guardado y llamar a la [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) método.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage! =_ nulo)  <br/> |Llame al método [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (similar al método OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) ) seguido de las acciones de **SaveCompleted** normales. Si **SaveCompleted** se realizó correctamente, escriba el estado Normal. De lo contrario, especifique el estado de [HandsOffAfterSave](handsoffaftersave-state.md) .  <br/> |Normal o HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Forma recursiva invocar el método **HandsOffMessage** en los mensajes incrustados o el método OLE **IPersistStorage::HandsOffStorage** en los objetos OLE incrustados. Liberar el objeto de mensaje y los mensajes incrustados u objetos.  <br/> |HandsOffAfterSave  <br/> |
|**Guardar**, [IPersistMessage::InitNew](ipersistmessage-initnew.md)o [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Establece el último error y devolver E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devolver el último error.  <br/> |NoScribble  <br/> |
|Otros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos o métodos de otras interfaces  <br/> |Establece el último error y devolver E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Ver también



[Estados de formulario](form-states.md)

