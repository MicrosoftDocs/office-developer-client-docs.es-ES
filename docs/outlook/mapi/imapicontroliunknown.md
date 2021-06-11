---
title: IMAPIControl IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl
api_type:
- COM
ms.assetid: 5a647e15-ba22-4a7c-b235-75cd76b77c1a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8dce1415ef8d18f4b786e92324c888f9a0845162
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414042"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Habilita y deshabilita un control de botón y realiza tareas cuando un usuario de una aplicación cliente hace clic en el control habilitado. Los proveedores de servicios implementan objetos de control para crear botones personalizados en cuadros de diálogo, como hojas de propiedades de configuración, que se definen mediante tablas para mostrar. 
  
Para obtener más información acerca de cómo trabajar con tablas para mostrar y objetos de control, vea [Mostrar tablas](display-tables.md).
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuesto por:  <br/> |Objetos de control  <br/> |
|Implementado por:  <br/> |Proveedores de servicios  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIControl  <br/> |
|Tipo de puntero:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error de control de botón anterior.  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |Realiza una tarea como mostrar un cuadro de diálogo o iniciar una operación mediante programación cuando un usuario de la aplicación cliente hace clic en el control de botón.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Recupera un valor que indica si el control de botón está habilitado o deshabilitado.  <br/> |
   
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

