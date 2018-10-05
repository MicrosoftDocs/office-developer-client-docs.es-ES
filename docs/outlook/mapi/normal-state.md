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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395794"
---
# <a name="normal-state"></a>Estado normal

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
El estado Normal es donde el objeto de formulario dedica gran parte de su tiempo de espera para que las aplicaciones de cliente iniciar una acción, como guardar los cambios o cerrar el formulario. En la siguiente tabla se describe permitidos las transiciones de estado Normal.
  
|**IPersistMessage (método)**|**Acción**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md) (_pMessage ==_ NULL, _fSameAsLoad ==_ es TRUE)  <br/> o bien -  <br/> **IPersistMessage::Save** (_pMessage! =_ NULL, _fSameAsLoad ==_ FALSE)  <br/> |Forma recursiva guardar objetos OLE incrustados que se han modificado. Guardar los datos de mensaje en el objeto de mensaje. Almacenar la marca _fSameAsLoad_ para usarlo más adelante en el estado de [NoScribble](noscribble-state.md) .  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save** (_pMessage! =_ NULL, _fSameAsLoad ==_ es TRUE)  <br/> |Esto es el mismo que el caso anterior, excepto en que esta llamada **Guardar** se usa en situaciones de memoria baja y no debe producir un error por falta de memoria.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Forma recursiva invocar el método **HandsOffMessage** en los mensajes incrustados o el método OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) en los objetos OLE incrustados. Liberar el objeto de mensaje y los mensajes incrustados u objetos.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Establece el último error y devolver E_UNEXPECTED.  <br/> |Importance  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devolver el último error.  <br/> |Importance  <br/> |
|Otros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos o métodos de otras interfaces  <br/> |Implementar como se describe en la documentación de la [IPersistMessage: IUnknown](ipersistmessageiunknown.md) interfaz.  <br/> |Importance  <br/> |
   
## <a name="see-also"></a>Vea también



[Estados de formulario](form-states.md)

