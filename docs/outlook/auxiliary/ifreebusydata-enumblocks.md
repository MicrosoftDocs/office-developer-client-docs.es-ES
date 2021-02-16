---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: Obtiene una interfaz que enumera los bloques de datos de disponibilidad de un usuario dentro de un intervalo de tiempo especificado.
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317559"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

Obtiene una interfaz que enumera los bloques de datos de disponibilidad de un usuario dentro de un intervalo de tiempo especificado.
  
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
  
> [salida] Una interfaz para enumerar bloques de disponibilidad.
    
_ftmStart_
  
> [entrada] La hora de inicio de la enumeración. Se expresa en [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx).
    
_ftmEnd_
  
> [entrada] Hora de finalización de la enumeración. Se expresa en **FILETIME**. 
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Este método se usa para indicar el intervalo de tiempo de los elementos del calendario para los que se recuperarán los detalles. Los valores de  *ftmStart* y *ftmEnd* se almacenan en caché y se devuelven en una llamada posterior de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
Un proveedor de disponibilidad también puede usar posteriormente la interfaz [IEnumFBBlock](ienumfbblock.md) devuelta para obtener acceso a la enumeración. 
  
## <a name="see-also"></a>Consulte también

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)

