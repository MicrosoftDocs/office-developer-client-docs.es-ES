---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fd2575d401aa8a39d6f3b2cd08377b587b430ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817271"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Hace referencia a**: Outlook 
  
Permite que los servidores de formulario para recibir notificaciones de los visores del formulario. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Expuestos por:  <br/> |Formulario de aviso receptor objetos  <br/> |
|Se implementa mediante:  <br/> |Servidores de formulario  <br/> |
|Llamado por:  <br/> |Visores de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Indica que se ha producido un cambio en el estado del Visor del formulario.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Indica si el formulario puede controlar la clase de mensaje del mensaje siguiente para mostrar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Uso de servidores de formulario un formulario de aviso objeto receptor para implementar **IMAPIFormAdviseSink** en lugar de incluir con su objeto de formulario. Por lo tanto, los visores de formulario deben esperar un error de la llamada al método [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) de un formulario para obtener un puntero a esta interfaz. 
  
Formulario servidores llamar [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) al método de un visor registrar para recibir notificaciones. Un puntero a su implementación de **IMAPIFormAdviseSink** se incluye como un parámetro. 
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

