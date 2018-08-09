---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: Establece el intervalo de tiempo para una enumeración de libre/ocupado de bloques de datos para un usuario.
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816109"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

Establece el intervalo de tiempo para una enumeración de libre/ocupado de bloques de datos para un usuario.
  
## <a name="quick-info"></a>Información rápida

Vea [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Parámetros

_rtmStart_
  
> [entrada] Un valor de tiempo relativo para el inicio de la información de libre/ocupado. Este valor es el número de minutos desde el 1 de enero de 1601.
    
_rtmEnd_
  
> [entrada] Un valor de tiempo relativo para el final de la información de libre/ocupado. Este valor es el número de minutos desde el 1 de enero de 1601.
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Este método se usa para indicar el intervalo de tiempo de los elementos del calendario para el que se va a recuperar detalles. Los valores de *ftmStart* y *ftmEnd* se almacena en caché y se devuelven en una llamada posterior de [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md).
  
## <a name="see-also"></a>Vea también

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)

