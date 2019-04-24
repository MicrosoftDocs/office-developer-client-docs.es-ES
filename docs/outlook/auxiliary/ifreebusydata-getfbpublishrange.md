---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: Obtiene un intervalo de tiempo preestablecido para una enumeración de bloques de disponibilidad de datos para un usuario.
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317531"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

Obtiene un intervalo de tiempo preestablecido para una enumeración de bloques de disponibilidad de datos para un usuario.
  
## <a name="quick-info"></a>Información rápida

Consulte [IFreeBusyData](ifreebusydata.md).
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>Parameters

_prtmStart_
  
> contempla Un valor de tiempo relativo para el inicio de la información de disponibilidad. Este valor es el número de minutos transcurridos desde el 1 de enero de 1601.
    
_prtmEnd_
  
> contempla Un valor de tiempo relativo para el fin de la información de disponibilidad. Este valor es el número de minutos transcurridos desde el 1 de enero de 1601.
    
## <a name="return-values"></a>Valores devueltos

S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.
  
## <a name="remarks"></a>Comentarios

Un proveedor de disponibilidad llama a [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) o [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) para establecer el intervalo de tiempo de una enumeración. Si no se ha llamado a [IFreeBusyData:: EnumBlocks](ifreebusydata-enumblocks.md) o [IFreeBusyData:: SetFBRange](ifreebusydata-setfbrange.md) , los valores predeterminados para **prtmStart** y **prtmEnd** deben estar establecidos entre el 1 de abril de 1601 00:00:00Z y el 31 de agosto de 4500 11:59:59Z poco. Además, no debe establecer la hora de inicio para que sea mayor que la hora de finalización. 
  
**IFreeBusyData:: GetFBPublishRange** debe devolver los valores almacenados en caché para el intervalo de tiempo establecido por la llamada más reciente para **IFreeBusyData:: EnumBlocks** o **IFreeBusyData:: SetFBRange**. 
  
## <a name="see-also"></a>Vea también

- [Utilizar un tiempo relativo a los datos de disponibilidad de acceso](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

