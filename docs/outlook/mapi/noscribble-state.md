---
title: Estado nocribible
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326204"
---
# <a name="noscribble-state"></a>Estado nocribible

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado NoScribble indica que se están guardando los cambios en un mensaje. El guardado real de valores almacenados en la interfaz de usuario del objeto de formulario se produce cuando la aplicación cliente llama al método [IPersistMessage::Save](ipersistmessage-save.md) del objeto de formulario. En la tabla siguiente se describen las transiciones permitidas desde el estado NoScribble. 
  
|Método IPersistMessage**|**Action**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)  <br/> |Si la marca _fSameAsLoad_ era TRUE en la llamada [IPersistMessage::Save](ipersistmessage-save.md) que hizo que el formulario entrara en el estado NoScribble y el mensaje se haya modificado, marque internamente los cambios como guardados y llame al método [IMAPIViewAdviseSink::OnSaved.](imapiviewadvisesink-onsaved.md)  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)  <br/> |Llama al [método IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (similar al método OLE [IPersistStorage::HandsOffStorage)](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) seguido de las **acciones SaveCompleted** normales. Si **SaveCompleted** se ha realizado correctamente, escriba el estado Normal. De lo contrario, escriba el [estado HandsOffAfterSave.](handsoffaftersave-state.md)  <br/> |Normal o HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Invoca de forma recursiva el **método HandsOffMessage** en mensajes incrustados o el método OLE **IPersistStorage::HandsOffStorage** en objetos OLE incrustados. Libere el objeto message y los mensajes u objetos incrustados.  <br/> |HandsOffAfterSave  <br/> |
|**Save**, [IPersistMessage::InitNew](ipersistmessage-initnew.md)o [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Establece el último error en y devuelve E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devuelve el último error.  <br/> |NoScribble  <br/> |
|Otros [métodos o métodos IPersistMessage: IUnknown](ipersistmessageiunknown.md) de otras interfaces  <br/> |Establece el último error en y devuelve E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>Vea también



[Estados del formulario](form-states.md)

