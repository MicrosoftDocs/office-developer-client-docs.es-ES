---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Devuelve, para cada usuario especificado, una interfaz para enumerar los bloques de disponibilidad de datos dentro de un intervalo de tiempo.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319407"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Devuelve, para cada usuario especificado, una interfaz para enumerar los bloques de disponibilidad de datos dentro de un intervalo de tiempo. 
  
## <a name="quick-info"></a>Información rápida

Consulte [IFreeBusySupport](ifreebusysupport.md).
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>Parameters

_cMax_
  
> a Número de interfaces de [IFreeBusyData](ifreebusydata.md) que se devolverán. 
    
_rgfbuser_
  
> a La matriz de usuarios de disponibilidad para el que se recuperarán los datos.
    
_prgfbdata_
  
> a contempla Matriz de interfaces de **IFreeBusyData** que corresponden a la matriz _Rgfbuser_ de estructuras [FBUser](fbuser.md) . 
    
   > [!NOTE]
   > Esta matriz de punteros la asigna el autor de la llamada y la libera el autor de la llamada. Las interfaces reales que apuntan se sueltan cuando el autor de la llamada se hace con ellas. 
  
_phrStatus_
  
> contempla La matriz de **HRESULT** produce la recuperación de cada interfaz **IFreeBusyData** correspondiente. El valor puede ser NULL. Un resultado se establece en S_OK si la _prgfbdata_ correspondiente es válida. 
    
_pcRead_
  
>  contempla El número real de usuarios para los que se ha encontrado una interfaz **IFreeBusyData** . 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="see-also"></a>Vea también

- [Constantes (API de disponibilidad)](constants-free-busy-api.md)

