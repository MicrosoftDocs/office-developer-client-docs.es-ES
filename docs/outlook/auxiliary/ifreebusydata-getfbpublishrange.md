---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtiene un intervalo de tiempo preestablecido para una enumeración de bloques de disponibilidad de datos para un usuario.
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816091"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Obtiene un intervalo de tiempo preestablecido para una enumeración de bloques de disponibilidad de datos para un usuario.
  
## <a name="quick-info"></a>Información rápida

Vea [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Parámetros

_prtmStart_
  
> [out] Un valor de tiempo relativo para el inicio de la información de libre/ocupado. Este valor es el número de minutos desde el 1 de enero de 1601.
    
_prtmEnd_
  
> [out] Un valor de tiempo relativo para el final de la información de libre/ocupado. Este valor es el número de minutos desde el 1 de enero de 1601.
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Notas

Llama a un proveedor de libre/ocupado [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) o [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) para establecer el intervalo de tiempo para una enumeración. Si no se ha llamado [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) o [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) , se deben establecer los valores predeterminados para **prtmStart** y **prtmEnd** entre el 1 de abril de 1601 00:00:00Z y el 31 de agosto de 4500 11:59:59Z respectivamente. Además, no debe establecer la hora de inicio para ser mayor que la hora de finalización. 
  
**IFreeBusyData::GetFBPublishRange** debe devolver que los valores almacenados en caché para el intervalo de tiempo establecen por la llamada más reciente para **IFreeBusyData::EnumBlocks** o **IFreeBusyData::SetFBRange**. 
  
## <a name="see-also"></a>Vea también

- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

