---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317629"
---
# <a name="ienumfbblock"></a>IEnumFBBlock

Admite el acceso y la enumeración de bloques de datos de disponibilidad de un usuario dentro de un intervalo de tiempo.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Suministrado por:  <br/> |Proveedor de disponibilidad  <br/> |
|Identificador de interfaz:  <br/> |**IEnumFBBlock** <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[Next](ienumfbblock-next.md) <br/> |Obtiene el siguiente número especificado de bloques de datos de disponibilidad en una enumeración.  <br/> |
|[Skip](ienumfbblock-skip.md) <br/> |Omite un número especificado de bloques de datos de disponibilidad.  <br/> |
|[Reset](ienumfbblock-reset.md) <br/> |Restablece el enumerador estableciendo el cursor al principio.  <br/> |
|[Clone](ienumfbblock-clone.md) <br/> |Crea una copia del enumerador, con la misma restricción de tiempo pero estableciendo el cursor al principio del enumerador.  <br/> |
|[Restrict](ienumfbblock-restrict.md) <br/> |Restringe la enumeración a un período de tiempo especificado.  <br/> |
   
## <a name="remarks"></a>Comentarios

Una enumeración contiene bloques de disponibilidad de datos que no se superponen en el tiempo. Cuando hay elementos superpuestos en un calendario, Outlook combina estos elementos para formar bloques de disponibilidad no superpuestos en la enumeración en función de este orden de prioridad: fuera de la oficina, ocupado, provisional.
  
Un proveedor de disponibilidad obtiene esta interfaz y la enumeración de un intervalo de tiempo para un usuario a través de [IFreeBusyData](ifreebusydata.md).
  
## <a name="see-also"></a>Consulte también

- [Información sobre la API de disponibilidad](about-the-free-busy-api.md)  
- [Constantes (API de disponibilidad)](constants-free-busy-api.md)  
- [IFreeBusyData](ifreebusydata.md)

