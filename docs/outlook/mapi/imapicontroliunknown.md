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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 395e44c2ea54816fab9f29dbedfe5e165e98c7b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817207"
---
# <a name="imapicontrol--iunknown"></a>IMAPIControl: IUnknown

  
  
**Se aplica a**: Outlook 
  
Habilita y deshabilita un control de botón y realiza tareas cuando un usuario de una aplicación de cliente hace clic en el control habilitado. Proveedores de servicios de implementan objetos de control para crear botones personalizados en los cuadros de diálogo, como las hojas de propiedades de configuración, que se definen mediante el uso de las tablas para mostrar. 
  
Para obtener más información acerca de cómo trabajar con tablas para mostrar y controlar objetos, vea [Mostrar tablas](display-tables.md).
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Expuestos por:  <br/> |Objetos de control  <br/> |
|Se implementa mediante:  <br/> |Proveedores de servicios  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIControl  <br/> |
|Tipo de puntero:  <br/> |LPMAPICONTROL  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[GetLastError](imapicontrol-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error de control de botón anterior.  <br/> |
|[Activate](imapicontrol-activate.md) <br/> |Realiza una tarea como mostrar un cuadro de diálogo o iniciar una operación de programación cuando un usuario de la aplicación cliente hace clic en el control de botón.  <br/> |
|[GetState](imapicontrol-getstate.md) <br/> |Recupera un valor que indica si el control de botón está habilitado o deshabilitado.  <br/> |
   
## <a name="see-also"></a>Ver también



[Interfaces MAPI](mapi-interfaces.md)

