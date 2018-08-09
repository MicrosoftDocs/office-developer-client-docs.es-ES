---
title: IFreeBusyData
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c9a80ad3-6311-fe07-b6f7-9fd63424753b
ms.openlocfilehash: aa42561277d5fc4de93eeedec8ceb6f36530fb80
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816097"
---
# <a name="ifreebusydata"></a>IFreeBusyData

Para un usuario determinado, obtiene y establece un intervalo de tiempo y devuelve una interfaz para enumerar los bloques de libre/ocupado de datos dentro de este intervalo de tiempo.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Hereda de:  <br/> |[IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Suministrado por:  <br/> |Proveedor de libre/ocupado  <br/> |
|Identificador de interfaz:  <br/> |IID_IFreeBusyData  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[Placeholder1](ifreebusydata-placeholder1.md) <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
|[EnumBlocks](ifreebusydata-enumblocks.md) <br/> |Obtiene una interfaz que se enumera los bloques de disponibilidad de datos para un usuario dentro de un intervalo de tiempo especificado.  <br/> |
|[Placeholder2](ifreebusydata-placeholder2.md) <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
|[Placeholder3](ifreebusydata-placeholder3.md) <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
|[Placeholder4](ifreebusydata-placeholder4.md) <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
|[Placeholder5](ifreebusydata-placeholder5.md) <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
|[SetFBRange](ifreebusydata-setfbrange.md) <br/> |Establece el intervalo de tiempo para una enumeración de libre/ocupado de bloques de datos para un usuario.  <br/> |
|[Placeholder6](ifreebusydata-placeholder6.md) <br/> | *Este miembro es un marcador de posición y no se admite.*  <br/> |
|[GetFBPublishRange](ifreebusydata-getfbpublishrange.md) <br/> |Obtiene un intervalo de tiempo preestablecido para una enumeración de bloques de disponibilidad de datos para un usuario.  <br/> |
   
## <a name="remarks"></a>Comentarios

La mayoría de los miembros de esta interfaz es marcadores de posición reservados para el uso interno de Outlook y está sujetos a cambios. Proveedores de libre/ocupado deben implementarlos únicamente como se especifica, devolver que valores devueltos sólo especificado.
  
## <a name="see-also"></a>Vea también

- [Información sobre la API de disponibilidad](about-the-free-busy-api.md)
- [Constantes (API de libre/ocupado)](constants-free-busy-api.md)

