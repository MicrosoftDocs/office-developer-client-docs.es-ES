---
title: IUnknown IMAPIFormAdviseSink
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
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286607"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite que los servidores de formularios reciban notificaciones de visores de formulario. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
|Expuesto por:  <br/> |Notificar a los objetos de receptor de formulario  <br/> |
|Implementado por:  <br/> |Servidores de formulario  <br/> |
|Llamado por:  <br/> |Visores de formularios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Indica que se ha producido un cambio en el estado del visor de formularios.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Indica si el formulario puede controlar la clase de mensaje del siguiente mensaje que se va a mostrar.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los servidores de formularios usan un objeto Sink de notificaciones de formulario para implementar **IMAPIFormAdviseSink** en lugar de incluirlos con el objeto Form. Por lo tanto, los visores de formulario deben esperar una llamada fallida al método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de un formulario para obtener un puntero a esta interfaz. 
  
Los servidores de formularios llaman al método [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) del visor para registrarse en las notificaciones. Un puntero a su implementación de **IMAPIFormAdviseSink** se incluye como parámetro. 
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

