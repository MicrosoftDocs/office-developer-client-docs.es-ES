---
title: IUnknown IMAPIOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321269"
---
# <a name="imapioffline--iunknown"></a>IMAPIOffline : IUnknown

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona información para un objeto sin conexión.
  
|||
|:-----|:-----|
|Suministrado por:  <br/> |Consulta en [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) <br/> |
|Llamado por:  <br/> |Client  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIOffline  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|**[SetCurrentState](imapioffline-setcurrentstate.md)** <br/> |Establece el estado actual de un objeto sin conexión en en línea o sin conexión.  <br/> |
|**[GetCapabilities](imapioffline-getcapabilities.md)** <br/> |Obtiene las condiciones para las que se admiten las devoluciones de llamada por un objeto sin conexión.  <br/> |
|**[GetCurrentState](imapioffline-getcurrentstate.md)** <br/> |Obtiene el estado en línea o sin conexión actual de un objeto sin conexión.  <br/> |
| *Marcador de posición de miembro*  <br/> |Este miembro es un marcador de posición y no es compatible.  <br/> |
   
## <a name="remarks"></a>Comentarios

Un cliente usa **[HrOpenOfflineObj](hropenofflineobj.md)** para abrir y obtener un objeto sin conexión que admita **IMAPIOfflineMgr**. Debido a que **IMAPIOfflineMgr** se hereda de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), el cliente puede consultar esta interfaz (mediante [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) para obtener un puntero al puntero de interfaz para **IMAPIOffline** para el objeto sin conexión. A continuación, el cliente puede obtener o establecer el estado actual del objeto o averiguar sobre las funciones de devolución de llamada del objeto (llamando a **IMAPIOffline:: GetCapabilities** ) y elegir la configuración de las devoluciones de llamada mediante **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**. 
  
Un miembro de esta interfaz es un marcador de posición reservado para el uso interno de Microsoft Outlook 2013 y está sujeto a cambios. Los demás miembros de esta interfaz solo deben usarse como documentados. 
  
## <a name="see-also"></a>Vea también



[IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md)


[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Interfaces MAPI](mapi-interfaces.md)

