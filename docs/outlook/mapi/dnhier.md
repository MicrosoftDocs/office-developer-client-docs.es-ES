---
title: DNHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3953dc9d-0146-3689-63f0-c6ba78566b8b
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 3c7d59849fcd66a5fe90623b7bb8516d13b4a2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816722"
---
# <a name="dnhier"></a>DNHIER

**Hace referencia a**: Outlook 
  
Información para la descarga de una jerarquía desde el servidor durante el [estado de la jerarquía de descarga](download-hierarchy-state.md), que forma parte de una sincronización completa de jerarquía. Este proceso de descarga utiliza sincronización de cambio Incremental (ICS) de Microsoft Exchange. Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
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

## <a name="members"></a>Members

_ulFlags_
  
>  [entrada] Marcas para determinar el comportamiento adecuado durante la descarga. 
    
   - DNH_OK
    
   - [entrada] Descarga fue correcta. El cliente establece esto después de descargar información desde el servidor.
    
_pstmReserved_
  
> [out] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_pxihc_
  
>  [out] Puntero a la interfaz de jerarquía de **IExchangeImportHierarchyChanges** que admite la descarga de los cambios incrementales de jerarquía. Para obtener más información sobre **IExchangeImportHierarchyChanges**, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_cEntNew_
  
> [out] Número de carpetas agregadas al almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
_cEntMod_
  
> [out] Número de carpetas que desea modificar en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
_cEntDel_
  
> [out] Número de carpetas que desea eliminar en el almacén local. Outlook rellena este valor durante la descarga al usar ICS.
    
## <a name="see-also"></a>Vea también

- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md) 
- [Constantes MAPI](mapi-constants.md)

