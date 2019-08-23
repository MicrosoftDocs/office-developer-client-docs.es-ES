---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: 4716a6f42968d7451a5db36173c4e6a9e843c08e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337005"
---
# <a name="dntbl"></a>DNTBL
 
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Información para descargar el contenido de una carpeta del servidor durante el [estado descargar tabla](download-table-state.md), como parte de una sincronización completa para el contenido de un almacén.
  
## <a name="quick-info"></a>Información rápida

```cpp
struct DNTBL 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved1; 
    LPSTREAM pstmReserved2; 
    LPSTREAM pstmReserved3; 
    LPSTREAM pstmReserved4; 
    PXICC pxicc; 
    PXIHC pxihc; 
    LPSTR pszName; 
    FILETIME ftLastMod; 
    ULONG ulRights; 
    FEID feid; 
    UINT uintReserved; 
    DNTBLE rgte[2]; 
    LPSRestriction psrReserved; 
    BOOL boReserved; 
    void* pReserved1; 
    void* pReserved2; 
};

```

## <a name="members"></a>Miembros

_ulFlags_
  
> [entrada] Marcadores para modificar el comportamiento. 
    
  - DNT_OK
    
    - [entrada] La descarga se ha completado correctamente. El cliente lo establece después de descargar la información del servidor.
    
_pstmReserved1_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pstmReserved2_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pstmReserved3_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pstmReserved4_
  
> [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pxicc_
  
>  [salida] Puntero a la interfaz de contenido **IExchangeImportContentsChanges** que admite la descarga de cambios en el contenido. Para más información sobre **IExchangeImportContentsChanges**, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pxihc_
  
>  [salida] Puntero a la interfaz de contenido **IExchangeImportHierarchyChanges** que admite la descarga de los cambios de jerarquía incremental. Para más información sobre **IExchangeImportHierarchyChanges**, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_pszName_
  
>  [salida] Nombre de la carpeta. 
    
_ftLastMod_
  
>  [salida] Última vez que se modificó la carpeta. 
    
_ulRights_
  
>  [salida] Valor de la propiedad **[PR_RIGHTS](https://msdn.microsoft.com/library/ee238052%28v=EXCHG.80%29.aspx)** de la carpeta. 
    
_feid_
  
>  [salida] Id. de entrada de la carpeta. 
    
_uintReserved_
  
>  [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_rgte_
  
> [salida] Cambios de elementos normales (o no ocultos) y asociados (ocultos).  *rgte[0]* es para elementos normales y *rgte[1]* para elementos asociados. Outlook rellena este miembro durante la descarga al usar la sincronización de cambio incremental (ICS). Para obtener más información sobre ICS, consulte [Criterios de evaluación ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_lpsrReserved_
  
>  [entrada] / [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_boReserved_
  
>  [entrada] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pReserved1_
  
>  [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pReserved2_
  
>  [entrada] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
## <a name="see-also"></a>Vea también

- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)  
- [Constantes MAPI](mapi-constants.md) 
- [DNTBLE](dntble.md)

