---
title: UPMOV
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 098743a5-f265-639a-8ba6-1412705bee0a
description: 'Última modificación: 05 de julio de 2012'
ms.openlocfilehash: a7588d5fed2e059be7e628d8a76a12f76aea734d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393386"
---
# <a name="upmov"></a>UPMOV
 
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Información para cargar los elementos que se han movido. Esta información se usa durante la [carga Eliminar estado](upload-delete-status-state.md) y [cargar el estado de la tabla](upload-table-state.md).
  
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
  
> [entrada] Marcas para determinar el comportamiento adecuado durante la carga.
    
  - UPV_ERROR
    
    - [entrada] Problema al abrir la carpeta del servidor.
    
  - UPV_DIRTY
    
    - [entrada] Ha cambiado el estado de carga. Esto se usa en el cliente para realizar un seguimiento el cambio de estado para el almacén local.
    
  - UPV_COMMIT
    
    - [entrada] Confirmar el estado de carga.
    
_Conserva_
  
>  [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pstmReserved_
  
>  [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pszName_
  
>  [out] Nombre de la carpeta de destino. 
    
  > [!NOTE]
  > Este miembro no es compatible con UNICODE. 
  
_feid_
  
>  [out] Identificador de entrada de la carpeta de destino. 
    
_pfld_
  
>  [entrada] Puntero a la carpeta del servidor. 
    
_pxicc_
  
>  [entrada] Puntero a la interfaz de contenido **IExchangeImportContentsChanges** que admite la carga de los cambios de contenido cuando se usa la sincronización de cambio Incremental (ICS). Para obtener más información sobre **IExchangeImportContentsChanges** y ICS, vea [Los criterios de evaluación de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
    
_dwReservado_
  
>  [salida] Este miembro está reservado para uso interno de Outlook y no es compatible. 
    
_pupmovNext_
  
>  [out] A continuación, mover contexto. 
    
_cEntMov_
  
>  [entrada] Número de elementos movidos aquí. 
    
## <a name="see-also"></a>Vea también

- [Información sobre la API de replicación](about-the-replication-api.md)
- [Información sobre la máquina de estados de replicación](about-the-replication-state-machine.md)
- [Constantes MAPI](mapi-constants.md)
- [FEID](feid.md)

