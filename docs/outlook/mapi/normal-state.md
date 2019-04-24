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
  
El estado normal es donde el objeto Form pasa la mayor parte del tiempo, esperando a las aplicaciones cliente iniciar una acción, como guardar los cambios o cerrar el formulario. En la tabla siguiente se describen las transiciones permitidas desde el estado normal.
  
|**Método IPersistMessage**|**Action**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage:: Save](ipersistmessage-save.md) (_pMessage = =_ null, _fSameAsLoad = =_ true)  <br/> O bien,  <br/> **IPersistMessage:: Save** (_pMessage! =_ null, _fSameAsLoad = =_ false)  <br/> |Guardar de forma recursiva todos los objetos OLE incrustados que se han modificado. Vuelva a guardar los datos del mensaje en el objeto de mensaje. Almacene la marca _fSameAsLoad_ para su uso posterior en el estado noscribble. [](noscribble-state.md)  <br/> |NoScribble  <br/> |
|**IPersistMessage:: Save** (_pMessage! =_ null, _fSameAsLoad = =_ true)  <br/> |Esto es lo mismo que el caso anterior, excepto que esta llamada a **Save** se usa en situaciones de memoria baja y no debe producir errores por falta de memoria.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Invoque de forma recursiva el método **HandsOffMessage** en mensajes incrustados o el método OLE [IPersistStorage:: HANDSOFFSTORAGE](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) en objetos OLE incrustados. Libere el objeto de mensaje y todos los mensajes u objetos incrustados.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md) o [IPersistMessage:: Load](ipersistmessage-load.md) <br/> |Establezca el último error en y devuelva E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devolver el último error.  <br/> |Normal  <br/> |
|Otros [IPersistMessage:](ipersistmessageiunknown.md) métodos o métodos IUnknown de otras interfaces  <br/> |Implemente como se describe en la documentación de la interfaz [IPersistMessage: IUnknown](ipersistmessageiunknown.md) .  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>Vea también



[Estados de formulario](form-states.md)

