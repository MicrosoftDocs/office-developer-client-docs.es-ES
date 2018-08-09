---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtiene una interfaz que se enumera los bloques de disponibilidad de datos para un usuario dentro de un intervalo de tiempo especificado.
ms.openlocfilehash: ab377b1029296b6b4bac68d7169dcf7b8dcd8b87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816096"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Obtiene una interfaz que se enumera los bloques de disponibilidad de datos para un usuario dentro de un intervalo de tiempo especificado.
  
## <a name="quick-info"></a>Información rápida

Vea [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>Parámetros

_ppenumfb_
  
> [out] Una interfaz para enumerar los bloques de libre/ocupado.
    
_ftmStart_
  
> [entrada] La hora de inicio para la enumeración. Se expresa en [FILETIME](http://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_ftmEnd_
  
> [entrada] La hora de finalización para la enumeración. Se expresa en **FILETIME**. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Este método se usa para indicar el intervalo de tiempo de los elementos del calendario para el que se va a recuperar detalles. Los valores de *ftmStart* y *ftmEnd* se almacena en caché y se devuelven en una llamada posterior de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
Un proveedor de libre/ocupado posteriormente también puede usar la interfaz de [IEnumFBBlock](ienumfbblock.md) devuelta para tener acceso a la enumeración. 
  
## <a name="see-also"></a>Vea también

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)

