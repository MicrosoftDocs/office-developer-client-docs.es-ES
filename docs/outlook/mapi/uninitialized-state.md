---
title: Estado no inicializado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425564"
---
# <a name="uninitialized-state"></a>Estado no inicializado

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El estado Uninitialized es el estado inicial en el que deben estar los objetos de formulario cuando se crean por primera vez. Los objetos form se inicializan con datos de mensaje cuando una aplicación cliente llama al método [IPersistMessage::InitNew](ipersistmessage-initnew.md) o [IPersistMessage::Load](ipersistmessage-load.md) en el objeto de formulario. En la tabla siguiente se describen las transiciones permitidas desde el estado Unitialized. 
  
|**Método IPersistMessage**|**Action**|**Nuevo estado**|
|:-----|:-----|:-----|
|[IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Cargue el objeto de formulario con datos predeterminados.  <br/> |[Normal](normal-state.md) <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Cargue el objeto de formulario con datos del mensaje de destino.  <br/> |Normal  <br/> |
|[IPersistMessage::GetClassID](ipersistmessage-getclassid.md) <br/> |Devolver correctamente o establecer el último error en y devolver E_UNEXPECTED.  <br/> |Sin inicializar  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Devuelve el último error.  <br/> |Sin inicializar  <br/> |
|Otros [métodos o métodos IPersistMessage: IUnknown](ipersistmessageiunknown.md) de otras interfaces  <br/> |Establece el último error en y devuelve E_UNEXPECTED.  <br/> |Sin inicializar  <br/> |
   
## <a name="see-also"></a>Vea también



[Estado normal](normal-state.md)
  
[Estados del formulario](form-states.md)

