---
title: Información sobre la API de recuperación de bloqueo de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: fbb6d22414daf3464e80fbf1d9cf92ccb3d560e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576592"
---
# <a name="about-the-mapi-crash-recovery-api"></a>Información sobre la API de recuperación de bloqueo de MAPI

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
La API de recuperación de MAPI se bloquee comprueba que el estado del archivo de carpetas personales (PST) o archivo de carpetas sin conexión (OST) de memoria para comprobar que los datos están en un estado coherente compartida. Si está en un estado coherente, la función [MAPICrashRecovery](mapicrashrecovery.md) mueve los datos de los archivos pst de abrir u ost en el disco y bloquea los archivos PST u ost y no permitir que cualquier lectura o acceso de escritura a los datos. Esto garantiza que los datos permanecen en un estado coherente hasta que se finalice el proceso. Al garantizar que los archivos PST u ost se encuentran en un estado coherente antes de que finalice el proceso, puede evitar que Microsoft Outlook 2013 y Microsoft Outlook 2010 muestre el siguiente mensaje de error y evitar problemas de rendimiento. 
  
 **Un archivo de datos no se cerró correctamente la última vez que se usó y que se está protegiendo para problemas. Podría verse afectado el rendimiento mientras la comprobación está en curso.**
  
Esta API ofrece lo siguiente:
  
Constantes:
  
- [Constantes MAPI](mapi-constants.md)
    
Funciones:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Vea también



[Usar la API de recuperación de bloqueo de MAPI](how-to-use-the-mapi-crash-recovery-api.md)

