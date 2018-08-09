---
title: IMAPIOfflineMgr IMAPIOffline
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr
api_type:
- COM
ms.assetid: 3e430308-190c-c9bb-fffc-c26ffecb73a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 644fad96c8aec3701233351469a84ef93341b397
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817399"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**Hace referencia a**: Outlook 
  
Admite registrar para realizar devoluciones de llamadas de notificación acerca de los cambios de estado de conexión de una cuenta de usuario.
  
|||
|:-----|:-----|
|Exportada por:  <br/> |Msmapi32.dll  <br/> |
|Se implementa mediante:  <br/> |Outlook  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Aviso](imapiofflinemgr-advise.md) <br/> |Registra para realizar devoluciones de llamadas de notificación acerca de los cambios de la conexión.  <br/> |
|[Desaconsejar](imapiofflinemgr-unadvise.md) <br/> |Quita un registro determinado para realizar devoluciones de llamadas de notificación.  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
   
## <a name="remarks"></a>Comentarios

Al abrir un objeto sin conexión para un perfil de cuenta de usuario con **[HrOpenOfflineObj](hropenofflineobj.md)**, un cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**. 
  
Debido a que esta interfaz hereda de **[IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx)**, el cliente puede consultar esta interfaz (mediante el uso de **[IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)** ) para obtener un objeto que admite **[IMAPIOffline](imapiofflineiunknown.md)**. El cliente puede, a continuación, obtenga información acerca de las funciones de devolución de llamada del objeto sin conexión (por llamada **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** ) y elija Configurar las devoluciones de llamada (mediante **IMAPIOfflineMgr::Advise** ). 
  
La mayoría de los miembros de esta interfaz es marcadores de posición reservados para el uso interno de Outlook y está sujetos a cambios. Los autores de llamadas de esta interfaz deben usar el marcador de posición que no sean miembros sólo tal como se documenta.
  
## <a name="see-also"></a>Vea también



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Interfaces MAPI](mapi-interfaces.md)

