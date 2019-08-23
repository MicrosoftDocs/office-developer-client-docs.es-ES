---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337117"
---
# <a name="dntble"></a>DNTBLE

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Información para descargar el contenido de una carpeta del servidor durante el [estado descargar tabla](download-table-state.md). Este proceso de descarga usa la sincronización de cambio incremental (ICS) de Microsoft Exchange. Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Información rápida

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Miembros

 _cEntNew_
  
> [salida] Número de elementos añadidos al almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
 _cEntMod_
  
> [salida] Número de elementos modificados en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
 _cEntRead_
  
> [salida] Número de elementos leídos o marcados como no leídos en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
 _cEntDel_
  
> [salida] Número de elementos eliminados en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
## <a name="see-also"></a>Vea también



[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[DNTBL](dntbl.md)

