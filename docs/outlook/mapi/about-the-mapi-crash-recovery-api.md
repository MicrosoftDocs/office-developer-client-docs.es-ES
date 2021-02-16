---
title: Información sobre la API de recuperación de bloqueo de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: bc1e1f55-1959-a4a9-a24d-f006af531c9a
description: '�ltima modificaci�n: lunes, 25 de junio de 2012'
ms.openlocfilehash: 1acca6d806c1734007ac7c5e41059d3a870dc5bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420265"
---
# <a name="about-the-mapi-crash-recovery-api"></a>Información sobre la API de recuperación de bloqueo de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
La API de recuperación de bloqueos mapi comprueba el estado de la memoria compartida del archivo de carpetas personales (PST) o del archivo de carpetas sin conexión (OST) para comprobar que los datos están en un estado coherente. Si se encuentra en un estado coherente, la función [MAPICrashRecovery](mapicrashrecovery.md) mueve los datos de los archivos PST u OST abiertos al disco y bloquea los archivos PST o OST y no permite ningún acceso de lectura o escritura a los datos. Esto garantiza que los datos permanezcan en un estado coherente hasta que finalice el proceso. Al asegurarse de que los ARCHIVOS OST están en un estado coherente antes de que finalice el proceso, puede evitar que Microsoft Outlook 2013 y Microsoft Outlook 2010 muestren el siguiente mensaje de error y evitar problemas de rendimiento. 
  
 **Un archivo de datos no se ha cerrado correctamente la última vez que se usó y se está buscando problemas. El rendimiento puede verse afectado mientras la comprobación está en curso.**
  
Esta API proporciona lo siguiente:
  
Constantes:
  
- [Constantes MAPI](mapi-constants.md)
    
Funciones:
  
- [MAPICrashRecovery](mapicrashrecovery.md)
    
## <a name="see-also"></a>Consulte también



[Usar la API de recuperación de bloqueo de MAPI](how-to-use-the-mapi-crash-recovery-api.md)

