---
title: IUnknown IMAPIViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406034"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Administra un formulario en el visor de formularios de una aplicación cliente. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
|Expuesto por:  <br/> |Objetos de contexto de vista  <br/> |
|Implementado por:  <br/> |Visores de formularios  <br/> |
|Llamado por:  <br/> |Objetos de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIViewContext  <br/> |
|Tipo de puntero:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Administra el registro de un formulario para recibir notificaciones sobre cambios en el visor.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Activa el mensaje siguiente o anterior en el visor de formularios.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Recupera la información de impresión actual.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Recupera una secuencia que se utilizará para guardar el mensaje actual.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Recupera el estado actual del visor.  <br/> |
|[Volvió](imapiviewcontext-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produce en el objeto de contexto de vista.  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

