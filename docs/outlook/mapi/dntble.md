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
ms.openlocfilehash: 51a79075dac62a051f5a28dbcb70e7d6ff200e65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816749"
---
# <a name="dntble"></a>DNTBLE

  
  
**Hace referencia a**: Outlook 
  
Información para descargar el contenido de una carpeta del servidor durante el [estado de la tabla de descarga](download-table-state.md). Este proceso de descarga utiliza sincronización de cambio Incremental (ICS) de Microsoft Exchange. Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
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

