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
ms.openlocfilehash: cee58299147c9f97ff61a3b8c460125349910637
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594463"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
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
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

