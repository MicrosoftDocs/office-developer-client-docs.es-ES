---
title: Estado HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426474"
---
# <a name="handsofffromnormal-state"></a>Estado HandsOffFromNormal

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado HandsOffFromNormal es muy similar al [estado HandsOffAfterSave.](handsoffaftersave-state.md) Forma parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente. Cuando se encuentra en este estado, el objeto form debe abstenerse de realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, ya que es posible que no haya otra oportunidad de guardar esos cambios. En la tabla siguiente se describen las transiciones permitidas desde el estado HandsOffFromNormal. 
  
|Método IPersistMessage**|**Action**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Reemplace el mensaje del objeto message por  _pMessage_, que es el reemplazo del mensaje revocado por la llamada anterior a [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md). Se garantiza que los datos del nuevo mensaje sean los mismos que en el mensaje revocado. El mensaje no debe marcarse como limpio ni se debe llamar a [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) después de esta llamada. Si la **llamada SaveCompleted** se realiza correctamente, escriba el [estado Normal.](normal-state.md) De lo contrario, permanezca en el estado HandsOffFromNormal.  <br/> |Normal o HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Establezca el último error en E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)o [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Establezca el último error en E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devuelve el último error.  <br/> |HandsOffFromNormal  <br/> |
|Otros [métodos o métodos IPersistMessage: IUnknown](ipersistmessageiunknown.md) de otras interfaces  <br/> |Establezca el último error en E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Vea también



[Estados del formulario](form-states.md)

