---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Devuelve, para cada usuario especificado, una interfaz para enumerar los bloques de libre/ocupado de datos dentro de un intervalo de tiempo.
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816094"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Devuelve, para cada usuario especificado, una interfaz para enumerar los bloques de libre/ocupado de datos dentro de un intervalo de tiempo. 
  
## <a name="quick-info"></a>Información rápida

Vea [IFreeBusySupport](ifreebusysupport.md).
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>Parámetros

_Cmáx_
  
> [entrada] El número de interfaces de [IFreeBusyData](ifreebusydata.md) para devolver. 
    
_rgfbuser_
  
> [entrada] La matriz de disponibilidad a los usuarios para recuperar datos.
    
_prgfbdata_
  
> [entrada] [out] La matriz de interfaces de **IFreeBusyData** que corresponden a la matriz _rgfbuser_ de estructuras [FBUser](fbuser.md) . 
    
   > [!NOTE]
   > Esta matriz de punteros es asignada por el autor de la llamada y libera el autor de la llamada. Las interfaces real que señala se liberan cuando el autor de la llamada se realiza con ellos. 
  
_phrStatus_
  
> [out] La matriz de resultados **HRESULT** para recuperar cada interfaz **IFreeBusyData** correspondiente. El valor puede ser NULL. Un resultado se establece en S_OK si correspondiente _prgfbdata_ es válida. 
    
_pcRead_
  
>  [out] El número real de los usuarios para el que se ha encontrado una interfaz **IFreeBusyData** . 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="see-also"></a>Vea también

- [Constantes (API de libre/ocupado)](constants-free-busy-api.md)

