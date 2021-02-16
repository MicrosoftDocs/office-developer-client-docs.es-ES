---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: cd9d4dffd83e1995319b0f0d661435fedb78f28c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317503"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Para un usuario determinado, obtiene y establece un intervalo de tiempo y devuelve una interfaz para enumerar bloques de datos de disponibilidad dentro de este intervalo de tiempo.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Suministrado por:  <br/> |Proveedor de disponibilidad  <br/> |
|Identificador de interfaz:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Orden de tabla virtual

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *Este miembro es un marcador de posición y no es compatible.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Obtiene una interfaz que enumera los bloques de datos de disponibilidad de un usuario dentro de un intervalo de tiempo especificado.  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *Este miembro es un marcador de posición y no es compatible.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Este miembro es un marcador de posición y no es compatible.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Este miembro es un marcador de posición y no es compatible.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Este miembro es un marcador de posición y no es compatible.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Establece el intervalo de tiempo para una enumeración de bloques de datos de disponibilidad de un usuario.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Este miembro es un marcador de posición y no es compatible.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Obtiene un intervalo de tiempo preestablecido para una enumeración de bloques de datos de disponibilidad de un usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

La mayoría de los miembros de esta interfaz son marcadores de posición reservados para el uso interno de Outlook y están sujetos a cambios. Los proveedores de disponibilidad solo deben implementarlos según lo especificado y devolver solo los valores devueltos especificados.
  
## <a name="see-also"></a>Consulte también

- [Información sobre la API de disponibilidad](about-the-free-busy-api.md)
- [Constantes (API de disponibilidad)](constants-free-busy-api.md)

