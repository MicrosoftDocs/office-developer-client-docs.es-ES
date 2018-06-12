---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Especifica dejar una copia de un mensaje en el servidor para una cuenta POP.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816324"
---
# <a name="proppopleaveonserver"></a>PROP_POP_LEAVE_ON_SERVER

Especifica dejar una copia de un mensaje en el servidor para una cuenta POP.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador:  <br/> |0 x 1000  <br/> |
|Tipo de propiedad:  <br/> |PT_DWORD  <br/> |
|Etiqueta de la propiedad:  <br/> |0x10000003  <br/> |
|Access:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Notas

En la siguiente tabla se enumera los valores posibles. Para obtener más información acerca de las constantes, vea [constantes (API de administración de cuenta)](constants-account-management-api.md) . 
  
|**Valores posibles**|**Descripción**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Deja una copia del mensaje en el servidor POP después de descargar el mensaje a un dispositivo.  <br/> |
|**REMOVE_AFTER** <br/> |Quita el mensaje del servidor POP después de descargar a un dispositivo.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Quita el mensaje del servidor POP sólo después de que el usuario elimina el mensaje de la carpeta Elementos eliminados.  <br/> |
|**GET_REMOVE_AFTER_DAYS** ( _ul_)  <br/> |Obtiene el número de días después de que el mensaje se quitará el servidor POP.  <br/> |
|**SET_REMOVE_AFTER_DAYS** ( _días_)  <br/> |Establece el número de días después de que el mensaje se quitará el servidor POP.  <br/> |
   
## <a name="see-also"></a>Ver también

- [Descargas de mensaje administración de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

