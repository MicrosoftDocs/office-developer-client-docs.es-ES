---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Especifica dejar una copia de un mensaje en el servidor para una cuenta POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410948"
---
# <a name="prop_pop_leave_on_server"></a>PROP_POP_LEAVE_ON_SERVER

Especifica dejar una copia de un mensaje en el servidor para una cuenta POP.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Identificador:  <br/> |0x1000  <br/> |
|Tipo de propiedad:  <br/> |PT_DWORD  <br/> |
|Etiqueta de propiedad:  <br/> |0x10000003  <br/> |
|Acceso:  <br/> |Solo lectura  <br/> |
   
## <a name="remarks"></a>Comentarios

En la tabla siguiente se enumeran los valores posibles. Vea [Constantes (API de administración de cuentas)](constants-account-management-api.md) para obtener más información sobre las constantes. 
  
|**Posibles valores**|**Descripción**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Deja una copia del mensaje en el servidor POP después de descargarlo en un dispositivo.  <br/> |
|**REMOVE_AFTER** <br/> |Quita el mensaje del servidor POP después de descargarlo en un dispositivo.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Quita el mensaje del servidor POP solo después de que el usuario elimine el mensaje de la carpeta Elementos eliminados.  <br/> |
|**GET_REMOVE_AFTER_DAYS**( _ul_)  <br/> |Obtiene el número de días después de los cuales se quitará el mensaje del servidor POP.  <br/> |
|**SET_REMOVE_AFTER_DAYS**( _días_)  <br/> |Establece el número de días después de los cuales se quitará el mensaje del servidor POP.  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Administrar la descarga de mensajes de las cuentas POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constantes (API de administración de cuenta)](constants-account-management-api.md)

