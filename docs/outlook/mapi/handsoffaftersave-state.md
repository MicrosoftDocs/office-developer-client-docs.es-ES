---
title: Estado de HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406608"
---
# <a name="handsoffaftersave-state"></a>Estado de HandsOffAfterSave

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado HandsOffAfterSave forma parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente. Cuando se encuentra en este estado, el objeto form debe abstenerse de realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, ya que es posible que no haya otra oportunidad de guardar esos cambios. En la tabla siguiente se describen las transiciones permitidas desde el estado HandsOffAfterSave.
  
|**Método IPersistMessage**|**Action**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Abra los objetos incrustados. Se garantiza que los datos del mensaje almacenado en  _pMessage_ sean los mismos que el mensaje de la llamada [IPersistMessage::Save](ipersistmessage-save.md) anterior. Si la **llamada SaveCompleted** se realiza correctamente, escriba el estado Normal. De lo contrario, establezca el último error en E_OUTOFMEMORY y permanezca en el estado HandsOffAfterSave.  <br/> |[Normal](normal-state.md) o HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Establezca el último error en E_INVALIDARG o E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save** o [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Establece el último error en y devuelve E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Cargue el objeto de formulario con datos del mensaje de destino. Esta llamada puede producirse cuando el objeto de formulario va al mensaje siguiente o anterior de una carpeta.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devuelve el último error.  <br/> |HandsOffAfterSave  <br/> |
|Otros [métodos o métodos IPersistMessage: IUnknown](ipersistmessageiunknown.md) de otras interfaces  <br/> |Establece el último error en y devuelve E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Vea también



[Estados del formulario](form-states.md)

