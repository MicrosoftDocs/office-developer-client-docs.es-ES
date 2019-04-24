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
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360504"
---
# <a name="uninitialized-state"></a>Estado sin inicializar

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado sin inicializar es el estado inicial en que los objetos de formulario deben estar en la primera vez que se crean. Los objetos de formulario se inicializan con los datos del mensaje cuando una aplicación cliente llama al método [IPersistMessage:: InitNew](ipersistmessage-initnew.md) o [IPersistMessage:: Load](ipersistmessage-load.md) en el objeto de formulario. En la tabla siguiente se describen las transiciones permitidas desde el estado Unitialized. 
  
|**Método IPersistMessage**|**Action**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Cargue el objeto Form con datos predeterminados.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Cargue el objeto de formulario con datos del mensaje de destino.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Devuelve Success o establece el último error en y devuelve E_UNEXPECTED.  <br/> |Sin inicializar  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devolver el último error.  <br/> |Sin inicializar  <br/> |
|Otros [IPersistMessage:](ipersistmessageiunknown.md) métodos o métodos IUnknown de otras interfaces  <br/> |Establezca el último error en y devuelva E_UNEXPECTED.  <br/> |Sin inicializar  <br/> |
   
## <a name="see-also"></a>Vea también



[Estado normal](normal-state.md)
  
[Estados de formulario](form-states.md)

