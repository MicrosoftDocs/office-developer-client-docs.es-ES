---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: Devuelve, para cada usuario especificado, una interfaz para enumerar bloques de datos de disponibilidad dentro de un intervalo de tiempo.
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411235"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

Devuelve, para cada usuario especificado, una interfaz para enumerar bloques de datos de disponibilidad dentro de un intervalo de tiempo. 
  
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

## <a name="parameters"></a>Parameters

_cMax_
  
> [in] Número de interfaces [IFreeBusyData](ifreebusydata.md) que se devolverán. 
    
_rgfbuser_
  
> [in] La matriz de usuarios de disponibilidad para la que se recuperarán los datos.
    
_prgfbdata_
  
> [in] [salida] Matriz de **interfaces IFreeBusyData** que corresponden a la matriz _rgfbuser_ de [estructuras FBUser.](fbuser.md) 
    
   > [!NOTE]
   > Esta matriz de punteros la asigna el autor de la llamada y la libera el autor de la llamada. Las interfaces reales a las que se apunta se liberan cuando el autor de la llamada ha terminado con ellas. 
  
_phrStatus_
  
> [salida] Matriz de **resultados HRESULT** para recuperar cada interfaz **IFreeBusyData** correspondiente. El valor puede ser NULL. Un resultado se establece en S_OK si  _prgfbdata correspondiente_ es válido. 
    
_pcRead_
  
>  [salida] Número real de usuarios para los que se ha encontrado una interfaz **IFreeBusyData.** 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="see-also"></a>Vea también

- [Constantes (API de disponibilidad)](constants-free-busy-api.md)

