---
title: Acerca de la última hora de actualización de una libreta de direcciones sin conexión
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: d8c554c5-89ac-9b32-5561-8d8178d2525a
description: Un sin conexión libreta de direcciones (OAB) proporciona a los usuarios de Outlook en un estado desconectado el acceso a información de directorio de la lista Global de direcciones (GAL) y de otras libretas de direcciones.
ms.openlocfilehash: b1e3ff012606615e5e962c400f86ab5ee2fbed83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816072"
---
# <a name="about-the-last-update-time-of-an-offline-address-book"></a>Acerca de la última hora de actualización de una libreta de direcciones sin conexión

Un sin conexión libreta de direcciones (OAB) proporciona a los usuarios de Outlook en un estado desconectado el acceso a información de directorio de la lista Global de direcciones (GAL) y de otras libretas de direcciones. Es una copia de una libreta de direcciones que Outlook ha descargado desde un servidor de Exchange para proporcionar acceso sin conexión.
  
Los administradores de Exchange pueden elegir qué libretas de direcciones que esté disponible para los usuarios que trabajan sin conexión. Para crear una copia de una libreta de direcciones, Exchange genera nuevos archivos OAB, comprime los archivos y ponerlos en un recurso compartido local. Dependiendo de la configuración de Outlook, Outlook descarga los archivos de OAB desde la Web o desde una carpeta pública a un equipo cliente para usar en un estado desconectado. Outlook comprueba para periódicamente y descargas de actualizaciones.
  
Soluciones de Outlook que desean proporcionar a sus usuarios acceso sin conexión a una OAB que necesite saber cuándo se actualizó por última vez la OAB desde el servidor de Exchange. Para buscar la última hora de actualización de una OAB, las soluciones pueden utilizar la siguiente entrada en el registro de Windows: **HKCU\Software\Microsoft\Exchange\Exchange Provider\OAB tiempo de última modificación**. El tipo de esta entrada del registro es **REG_BINARY**. Los datos están de 8 bytes de tamaño. Puede convertir los datos a una estructura [FILETIME](http://msdn.microsoft.com/library/9baf8a0e-59e3-4fbd-9616-2ec9161520d1%28Office.15%29.aspx) de 64 bits al especificar un valor de hora Universal coordinada (UTC) que Outlook descarga última los archivos de OAB desde el servidor de Exchange en el equipo cliente. 
  
## <a name="see-also"></a>Vea también

- [Managing Offline Address Books](http://msdn.microsoft.com/library/b7f26eca-b93b-4834-ba50-11febdefbb18.aspx)

