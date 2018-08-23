---
title: Estado sin inicializar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578251"
---
# <a name="uninitialized-state"></a>Estado sin inicializar

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado no inicializado es el formulario de estado inicial objetos deberían estar en cuando se crea por primera vez. Objetos de formulario se convierten en inicializar con datos de mensaje cuando una aplicación cliente llama al método [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load](ipersistmessage-load.md) en el objeto de formulario. La siguiente tabla describe las transiciones permitidas desde el estado Unitialized. 
  
|**IPersistMessage (método)**|**Acción**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Cargar el objeto de formulario con los datos predeterminados.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Cargar el objeto de formulario con datos desde el mensaje de destino.  <br/> |Importance  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Devolver un resultado correcto, o establece el último error y devolver E_UNEXPECTED.  <br/> |No inicializado  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devolver el último error.  <br/> |No inicializado  <br/> |
|Otros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos o métodos de otras interfaces  <br/> |Establece el último error y devolver E_UNEXPECTED.  <br/> |No inicializado  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[Estado normal](normal-state.md)
  
[Estados de formulario](form-states.md)

