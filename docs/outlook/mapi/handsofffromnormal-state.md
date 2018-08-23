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
ms.openlocfilehash: 92c604c621e2837b76e9e49fd182524ad17fbcac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588345"
---
# <a name="handsofffromnormal-state"></a>Estado HandsOffFromNormal

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado de HandsOffFromNormal es muy similar al estado [HandsOffAfterSave](handsoffaftersave-state.md) . Forma parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente. En este estado, el objeto de formulario debe evitar realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, porque puede que no haya otra oportunidad para guardar los cambios. La siguiente tabla describe las transiciones permitidas desde el estado HandsOffFromNormal. 
  
|IPersistMessage ** (método) **|**Acción**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ nulo)  <br/> |Reemplazar el mensaje del objeto de mensaje con _pMessage_, que es el sustituto para el mensaje revocado por la llamada anterior a [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md). Los datos en el nuevo mensaje se garantiza que será el mismo que en el mensaje revocado. No se debe marcar el mensaje como limpio, ni debe llamarse [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) después de esta llamada. Si se realiza correctamente la llamada **SaveCompleted** , especifique el estado [Normal](normal-state.md) . De lo contrario, permanecer en el estado de HandsOffFromNormal.  <br/> |Normal o HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ==_ nulo)  <br/> |Establece el último error a E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)o [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Establece el último error a E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devolver el último error.  <br/> |HandsOffFromNormal  <br/> |
|Otros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos o métodos de otras interfaces  <br/> |Establece el último error a E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Estados de formulario](form-states.md)

