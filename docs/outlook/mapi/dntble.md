---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391951"
---
# <a name="dntble"></a>DNTBLE

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Información para descargar el contenido de una carpeta del servidor durante el [estado de la tabla de descarga](download-table-state.md). Este proceso de descarga utiliza sincronización de cambio Incremental (ICS) de Microsoft Exchange. Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
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

## <a name="members"></a>Members

 _cEntNew_
  
> [out] Número de elementos que se agregan al almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
 _cEntMod_
  
> [out] Número de elementos modificados en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
 _cEntRead_
  
> [out] Número de elementos de lectura o marcados como no leído en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
 _cEntDel_
  
> [out] Número de elementos eliminados en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
## <a name="see-also"></a>Vea también



[Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
  
[Constantes MAPI](mapi-constants.md)
  
[DNTBL](dntbl.md)

