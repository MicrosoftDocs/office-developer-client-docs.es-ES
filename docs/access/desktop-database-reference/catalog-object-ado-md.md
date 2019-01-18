---
title: Catalog (objeto, ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0ee7d2e68df90c8eee4227f949f93ea074b7df97
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713092"
---
# <a name="catalog-object-ado-md"></a>Catalog (objeto, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Contiene información de esquema multidimensional (es decir, cubos y dimensiones subyacentes, jerarquías, niveles y elementos) específica de un proveedor de datos multidimensionales (MDP).

## <a name="remarks"></a>Comentarios

Con las colecciones y las propiedades de un objeto **Catalog**, puede hacer lo siguiente:

- Abrir el catálogo estableciendo la propiedad [ActiveConnection](activeconnection-property-ado-md.md) en un objeto [Connection](connection-object-ado.md) de ADO estándar o en una cadena de conexión válida.

- Identificar el **catálogo** con la propiedad [Name](name-property-ado-md.md).

- Recorrer en iteración los cubos de un catálogo mediante la colección [CubeDefs](cubedefs-collection-ado-md.md).

