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
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299527"
---
# <a name="handsoffaftersave-state"></a>Estado HandsOffAfterSave

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado HandsOffAfterSave forma parte del proceso de guardar el contenido de un formulario en un almacenamiento permanente. Cuando se encuentra en este estado, el objeto Form debe abstenerse de realizar cambios en las copias en memoria de los valores de las propiedades del mensaje, porque puede que no haya otra oportunidad para guardar los cambios. En la tabla siguiente se describen las transiciones permitidas desde el estado HandsOffAfterSave.
  
|**Método IPersistMessage**|**Action**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ null)  <br/> |Abra los objetos incrustados. Se garantiza que los datos del mensaje almacenados en _pMessage_ son los mismos que los del mensaje de la llamada anterior a [IPersistMessage:: Save](ipersistmessage-save.md) . Si la llamada **SaveCompleted** se realiza correctamente, escriba el estado normal. De lo contrario, establezca el último error en E_OUTOFMEMORY y manténgase en el estado HandsOffAfterSave.  <br/> |[Normal](normal-state.md) o HandsOffAfterSave  <br/> |
|**IPersistMessage:: SaveCompleted** (_pMessage = =_ null)  <br/> |Establezca el último error en E_INVALIDARG o E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**o [IPersistMessage:: InitNew](ipersistmessage-initnew.md) <br/> |Establezca el último error en y devuelva E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Cargue el objeto de formulario con datos del mensaje de destino. Esta llamada puede producirse cuando el objeto de formulario va al mensaje siguiente o anterior en una carpeta.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devolver el último error.  <br/> |HandsOffAfterSave  <br/> |
|Otros [IPersistMessage:](ipersistmessageiunknown.md) métodos o métodos IUnknown de otras interfaces  <br/> |Establezca el último error en y devuelva E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>Vea también



[Estados de formulario](form-states.md)

