---
title: Estado HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 274e7206171e1874e3625896952f861d25f3b382
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564538"
---
# <a name="handsoffaftersave-state"></a>Estado HandsOffAfterSave

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado de HandsOffAfterSave es parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente. En este estado, el objeto de formulario debe evitar realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, porque puede que no haya otra oportunidad para guardar los cambios. La siguiente tabla describe las transiciones permitidas desde el estado HandsOffAfterSave.
  
|**IPersistMessage (método)**|**Acción**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ nulo)  <br/> |Abrir objetos incrustados. Los datos en el mensaje que se almacenan en _pMessage_ se garantiza que será el mismo que el mensaje en la llamada [IPersistMessage::Save](ipersistmessage-save.md) anterior. Si se realiza correctamente la llamada **SaveCompleted** , especifique el estado Normal. En caso contrario, Establece el último error a E_OUTOFMEMORY y permanecer en el estado de HandsOffAfterSave.  <br/> |[Normal](normal-state.md) o HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ==_ nulo)  <br/> |Establece el último error E_INVALIDARG o E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Guardar**o [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Establece el último error y devolver E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Cargar el objeto de formulario con datos desde el mensaje de destino. Esta llamada puede producirse cuando el objeto de formulario se va al mensaje siguiente o anterior en una carpeta.  <br/> |Importance  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devolver el último error.  <br/> |HandsOffAfterSave  <br/> |
|Otros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos o métodos de otras interfaces  <br/> |Establece el último error y devolver E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Estados de formulario](form-states.md)

