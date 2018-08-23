---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b2aa08ea14df87f24cda3da0137ae4bfa2c50b40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576018"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Admite el uso de formularios configurables de tiempo de ejecución en entornos de sistemas distribuidos. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |MAPIForm.h  <br/> |
|Expuestos por:  <br/> |Objetos de generador de formulario  <br/> |
|Se implementa mediante:  <br/> |Servidores de formulario  <br/> |
|Llamado por:  <br/> |Visores de formulario  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFormFactory  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Devuelve un objeto de fábrica de clase para el formulario.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Devuelve una estructura [MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se producen al objeto de fábrica de formulario.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Mantiene un servidor de formulario abierto en la memoria.  <br/> |
   
## <a name="remarks"></a>Comentarios

La interfaz de **IMAPIFormFactory** se basa en la interfaz [IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) y los objetos que implementan **IMAPIFormFactory** también deben heredar de **IClassFactory**.
  
 **IMAPIFormFactory** es la interfaz que los visores de formulario que se usa para crear nuevos objetos de formulario cuando un servidor de formulario es compatible con más de una clase de mensaje (es decir, más de un tipo de objeto de formulario). 
  
## <a name="see-also"></a>Recursos adicionales



[Interfaces MAPI](mapi-interfaces.md)

