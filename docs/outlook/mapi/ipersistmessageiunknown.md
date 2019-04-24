---
title: IUnknown IPersistMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309607"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Permite a los visores de formularios controlar el almacenamiento de un formulario y realizar la transición entre los distintos Estados.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm. h  <br/> |
|Expuesto por:  <br/> |Objetos de mensajes persistentes  <br/> |
|Implementado por:  <br/> |Objetos de formulario  <br/> |
|Llamado por:  <br/> |Visores de formularios  <br/> |
|Identificador de interfaz:  <br/> |IID_IPersistMessage  <br/> |
|Tipo de puntero:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Volvió](ipersistmessage-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior en el objeto de formulario.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Devuelve un identificador que representa el servidor de formularios que puede administrar el formulario.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Comprueba el formulario en busca de cambios realizados desde la última vez que guardó.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Inicializa un mensaje nuevo.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Carga el formulario para un mensaje especificado.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Guarda un formulario revisado en el mensaje desde el que se ha cargado o creado.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Notifica al formulario que se ha completado una operación de guardado.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Hace que el formulario libere el mensaje actual.  <br/> |
   
## <a name="remarks"></a>Comentarios

Todos los formularios son necesarios para implementar la interfaz **IPersistMessage** . 
  
 **IPersistMessage** funciona de forma similar a la interfaz [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) OLE. Para obtener más información, consulte los métodos **IPersistStorage** . 
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

