---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: '�ltima modificaci�n: jueves, 5 de julio de 2012'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339189"
---
# <a name="upmov"></a>UPMOV
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Información para cargar los elementos que se han movido. Esta información se usa durante el estado de [carga de eliminación](upload-delete-status-state.md) y carga de la [tabla](upload-table-state.md).
  
## <a name="quick-info"></a>Información rápida

```cpp
struct UPMOV 
{ 
      ULONG          ulFlags; 
      LPVOID         pReserved; 
      LPSTREAM       pstmReserved; 
      LPSTR          pszName; 
      FEID           feid; 
      LPMAPIFOLDER   pfld; 
      PXICC          pxicc; 
      DWORD          dwReserved; 
      PUPMOV         pupmovNext; 
      UINT           cEntMov; 
};
```

## <a name="members"></a>Miembros

_ulFlags_
  
> a Marcas para determinar el comportamiento adecuado durante la carga.
    
  - UPV_ERROR
    
    - a Problema al abrir la carpeta del servidor.
    
  - UPV_DIRTY
    
    - a El estado de carga ha cambiado. El cliente lo usa para realizar un seguimiento del cambio en el estado del almacén local.
    
  - UPV_COMMIT
    
    - a Estado de carga de confirmación.
    
_Preserva_
  
>  [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pstmReserved_
  
>  [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pszName_
  
>  contempla Nombre de la carpeta de destino. 
    
  > [!NOTE]
  > Este miembro no es compatible con uniCODE. 
  
_feid_
  
>  contempla IDENTIFICADOR de entrada de la carpeta de destino. 
    
_pfld_
  
>  a Puntero a la carpeta del servidor. 
    
_pxicc_
  
>  a Puntero a la interfaz de contenido **IExchangeImportContentsChanges** que admite la carga de cambios de contenido al usar la sincronización de cambio incremental (ICS). Para obtener más información acerca de **IExchangeImportContentsChanges** e ICS, consulte [criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReserved_
  
>  [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pupmovNext_
  
>  contempla Siguiente contexto de movimiento. 
    
_cEntMov_
  
>  a Número de elementos movidos aquí. 
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)

