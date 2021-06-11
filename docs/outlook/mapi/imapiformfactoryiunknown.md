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
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342122"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Admite el uso de formularios en tiempo de ejecución configurables en entornos informáticos distribuidos. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiform.h  <br/> |
|Expuesto por:  <br/> |Objetos de fábrica de formularios  <br/> |
|Implementado por:  <br/> |Servidores de formulario  <br/> |
|Llamado por:  <br/> |Visores de formularios  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIFormFactory  <br/> |
|Tipo de puntero:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |Devuelve un objeto de fábrica de clase para el formulario.  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |Devuelve una [estructura MAPIERROR](mapierror.md) que contiene información sobre el error anterior que se produjo en el objeto de fábrica de formularios.  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |Mantiene un servidor de formulario abierto en la memoria.  <br/> |
   
## <a name="remarks"></a>Comentarios

La **interfaz IMAPIFormFactory** se basa en la interfaz [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) y los objetos que implementan **IMAPIFormFactory** también deben heredar de **IClassFactory**.
  
 **IMAPIFormFactory** es la interfaz que usan los visores de formulario para crear nuevos objetos de formulario cuando un servidor de formulario admite más de una clase de mensaje (es decir, más de un tipo de objeto de formulario). 
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

