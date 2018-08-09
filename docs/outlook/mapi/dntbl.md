---
title: DNTBL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 77835b48-43aa-8518-9712-754e84f1e713
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: 6096118d72dfc51fb60025a55f581ebf97b000a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816721"
---
# <a name="dntbl"></a>DNTBL
 
**Hace referencia a**: Outlook 
  
Información para descargar el contenido de una carpeta del servidor durante el [estado de la tabla de descarga](download-table-state.md), como parte de una sincronización completa para el contenido en un almacén.
  
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

## <a name="members"></a>Members

_ulFlags_
  
> [entrada] Indicadores para modificar el comportamiento 
    
  - DNT_OK
    
    - [entrada] Descarga fue correcta. El cliente establece esto después de descargar información desde el servidor.
    
_pstmReserved1_
  
> [out] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_pstmReserved2_
  
> [out] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_pstmReserved3_
  
> [out] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_pstmReserved4_
  
> [out] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_pxicc_
  
>  [out] Puntero a la interfaz de contenido de **IExchangeImportContentsChanges** que admite la descarga de cambios en el contenido. Para obtener más información sobre **IExchangeImportContentsChanges**, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_pxihc_
  
>  [out] Puntero a la interfaz de jerarquía de **IExchangeImportHierarchyChanges** que admite la descarga de los cambios incrementales de jerarquía. Para obtener más información sobre **IExchangeImportHierarchyChanges**, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_pszName_
  
>  [out] Nombre de la carpeta. 
    
_ftLastMod_
  
>  [out] Hora de última modificación de la carpeta. 
    
_ulRights_
  
>  [out] Valor de la propiedad **[PR_RIGHTS](http://msdn.microsoft.com/en-us/library/ee238052%28v=EXCHG.80%29.aspx)** de la carpeta. 
    
_feid_
  
>  [out] Identificador de entrada de la carpeta. 
    
_uintReserved_
  
>  [out] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_rgte_
  
> [out] Los cambios de normal (o no ocultos) y elementos asociados (u ocultos).  *rgte [0]* es para los elementos normales y *rgte [1]* es para los elementos asociados. Outlook rellena a este miembro durante la descarga, cuando se usa la sincronización de cambio Incremental (ICS). Para obtener más información acerca de ICS, vea [Los criterios de evaluación de ICS](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
    
_lpsrReserved_
  
>  [en] / [out] este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_boReserved_
  
>  [entrada] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_pReserved1_
  
>  [out] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
_pReserved2_
  
>  [entrada] Este miembro está reservado para el uso interno de Outlook y no se admite. 
    
## <a name="see-also"></a>Vea también

- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)  
- [Constantes MAPI](mapi-constants.md) 
- [DNTBLE](dntble.md)

