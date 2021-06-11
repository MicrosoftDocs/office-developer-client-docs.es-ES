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
ms.openlocfilehash: 235c2afb20e6f36df72eac4070c1df5fd10fcce8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270094"
---
# <a name="imapiofflinemgr--imapioffline"></a>IMAPIOfflineMgr : IMAPIOffline

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Admite el registro de devoluciones de llamada de notificación sobre los cambios de estado de conexión de una cuenta de usuario.
  
|||
|:-----|:-----|
|Exportada por:  <br/> |msmapi32.dll  <br/> |
|Implementado por:  <br/> |Outlook  <br/> |
|Llamado por:  <br/> |Cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIOfflineMgr  <br/> |
   
## <a name="vtable-order"></a>Orden de Vtable

|||
|:-----|:-----|
|[Aconsejar](imapiofflinemgr-advise.md) <br/> |Registra las devoluciones de llamada de notificación sobre los cambios de conexión.  <br/> |
|[Unadvise](imapiofflinemgr-unadvise.md) <br/> |Quita un registro determinado para las devoluciones de llamada de notificación.  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
| *Miembro de marcador de posición*  <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
   
## <a name="remarks"></a>Comentarios

Al abrir un objeto sin conexión para un perfil de cuenta de usuario mediante **[HrOpenOfflineObj](hropenofflineobj.md)**, un cliente obtiene un objeto sin conexión que admite **IMAPIOfflineMgr**. 
  
Dado que esta interfaz hereda de **[IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)** el cliente puede consultar esta interfaz (mediante **[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)** ) para obtener un objeto compatible con **[IMAPIOffline](imapiofflineiunknown.md)**. A continuación, el cliente puede averiguar las capacidades de devolución de llamada del objeto sin conexión (llamando a **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** ) y elegir configurar las devoluciones de llamada (mediante **IMAPIOfflineMgr::Advise** ). 
  
La mayoría de los miembros de esta interfaz son marcadores de posición reservados para el uso interno de Outlook y están sujetos a cambios. Los autores de llamadas de esta interfaz deben usar miembros que no son marcadores de posición solo como están documentados.
  
## <a name="see-also"></a>Vea también



[IMAPIOffline : IUnknown](imapiofflineiunknown.md)


[Información sobre la API de estado sin conexión](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[HrOpenOfflineObj](hropenofflineobj.md)
  
[Interfaces MAPI](mapi-interfaces.md)

