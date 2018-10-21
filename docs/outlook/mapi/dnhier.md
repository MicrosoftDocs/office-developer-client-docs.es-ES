---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: 06f30b4856fc10127aec99975652e28a5e8dda30
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389088"
---
# <a name="dnhier"></a>DNHIER

**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Información para descargar una jerarquía del servidor durante el [estado de descarga de jerarquía](download-hierarchy-state.md), que forma parte de la sincronización de jerarquía completa. Este proceso de descarga usa la sincronización de cambio incremental (ICS) de Microsoft Exchange. Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
## <a name="quick-info"></a>Información rápida

```cpp
struct DNHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    PXIHC pxihc; 
    UINT cEntNew; 
   UINT cEntMod; 
    UINT cEntDel; 
};
```

## <a name="members"></a>Miembros

_ulFlags_
  
>  [entrada] Indicadores para determinar el comportamiento adecuado durante la descarga. 
    
   - DNH_OK
    
   - [entrada] La descarga se ha completado correctamente. El cliente lo establece después de descargar la información del servidor.
    
_pstmReserved_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pxihc_
  
>  [salida] Puntero a la interfaz de contenido **IExchangeImportHierarchyChanges** que admite la descarga de los cambios de jerarquía incremental. Para más información sobre **IExchangeImportHierarchyChanges**, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_cEntNew_
  
> [salida] Número de carpetas añadidas al almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
_cEntMod_
  
> [salida] Número de carpetas que se modificarán en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
_cEntDel_
  
> [salida] Número de carpetas que se eliminarán en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
## <a name="see-also"></a>Vea también

- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md) 
- [Constantes MAPI](mapi-constants.md)

