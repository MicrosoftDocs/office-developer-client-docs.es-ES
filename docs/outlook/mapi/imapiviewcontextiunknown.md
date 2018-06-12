---
title: IMAPIViewContext IUnknown
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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: a7d62253baaaae7955e722874a15d05ed16e566e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817635"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext: IUnknown

  
  
**Se aplica a**: Outlook 
  
Administra un formulario en el Visor de formulario de la aplicación cliente. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Expuestos por:  <br/> |Objetos de contexto de vista  <br/> |
|Se implementa mediante:  <br/> |Visores de formulario  <br/> |
|Llamado por:  <br/> |Objetos de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIViewContext  <br/> |
|Tipo de puntero:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Administra el registro de un formulario para recibir las notificaciones sobre cambios en el Visor.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Activa el mensaje siguiente o anterior en el Visor de formulario.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Recupera información de impresión actual.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Recupera una secuencia que se utilizará para guardar el mensaje actual.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Recupera el estado actual del Visor.  <br/> |
|[GetLastError](imapiviewcontext-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen en el objeto de contexto de la vista.  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

