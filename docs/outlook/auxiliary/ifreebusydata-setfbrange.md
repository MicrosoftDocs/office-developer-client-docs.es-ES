---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Establece el intervalo de tiempo para una enumeración de bloques de disponibilidad de datos para un usuario.
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421665"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Establece el intervalo de tiempo para una enumeración de bloques de disponibilidad de datos para un usuario.
  
## <a name="quick-info"></a>Información rápida

Consulte [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Parameters

_rtmStart_
  
> a Un valor de tiempo relativo para el inicio de la información de disponibilidad. Este valor es el número de minutos transcurridos desde el 1 de enero de 1601.
    
_rtmEnd_
  
> a Un valor de tiempo relativo para el fin de la información de disponibilidad. Este valor es el número de minutos transcurridos desde el 1 de enero de 1601.
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Este método se usa para indicar el intervalo de tiempo de los elementos de calendario para los que se van a recuperar detalles. Los valores de *ftmStart* y *ftmEnd* se almacenan en caché y se devuelven en una llamada subsiguiente de [IFreeBusyData:: GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>Ver también

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)

