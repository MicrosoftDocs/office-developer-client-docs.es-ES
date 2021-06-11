---
title: Estado normal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335748"
---
# <a name="normal-state"></a>Estado normal

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado Normal es donde el objeto de formulario pasa la mayor parte del tiempo, a la espera de que las aplicaciones cliente inicien una acción como guardar cambios o cerrar el formulario. En la tabla siguiente se describen las transiciones permitidas desde el estado Normal.
  
|**Método IPersistMessage**|**Action**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> O bien,  <br/> **IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)  <br/> |Guarde de forma recursiva los objetos OLE incrustados que se hayan modificado. Vuelva a guardar los datos del mensaje en el objeto de mensaje. Almacene la _marca fSameAsLoad para_ su uso posterior en el [estado NoScribble.](noscribble-state.md)  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> |Esto es lo mismo que en el caso anterior, excepto que esta llamada **Guardar** se usa en situaciones de poca memoria y no debe fallar por falta de memoria.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Invoca de forma recursiva el **método HandsOffMessage** en mensajes incrustados o el método OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) en objetos OLE incrustados. Libere el objeto message y los mensajes u objetos incrustados.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Establece el último error en y devuelve E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devuelve el último error.  <br/> |Normal  <br/> |
|Otros [métodos o métodos IPersistMessage: IUnknown](ipersistmessageiunknown.md) de otras interfaces  <br/> |Implemente como se describe en la documentación de la [interfaz IPersistMessage : IUnknown.](ipersistmessageiunknown.md)  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>Vea también



[Estados del formulario](form-states.md)

