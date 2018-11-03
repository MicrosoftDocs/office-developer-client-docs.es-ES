---
title: Catalog (objeto, ADO MD)
TOCTitle: Catalog object (ADO MD)
ms:assetid: 708c4082-3589-7f3b-5ea3-f3705f3d3ff1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249445(v=office.15)
ms:contentKeyID: 48545559
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1dd402a27164b5fb40bab10d7809f042846e37b5
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943734"
---
# <a name="catalog-object-ado-md"></a>Catalog (objeto, ADO MD)


**Se aplica a**: Access 2013, Office 2013

Contiene información de esquema multidimensional (es decir, cubos y dimensiones subyacentes, jerarquías, niveles y elementos) específica de un proveedor de datos multidimensionales (MDP).

## <a name="remarks"></a>Comentarios

Con las colecciones y las propiedades de un objeto **Catalog**, puede hacer lo siguiente:

- Abrir el catálogo estableciendo la propiedad [ActiveConnection](activeconnection-property-ado-md.md) en un objeto [Connection](connection-object-ado.md) de ADO estándar o en una cadena de conexión válida.

- Identificar el **catálogo** con la propiedad [Name](name-property-ado-md.md).

- Recorrer en iteración los cubos de un catálogo mediante la colección [CubeDefs](cubedefs-collection-ado-md.md).

