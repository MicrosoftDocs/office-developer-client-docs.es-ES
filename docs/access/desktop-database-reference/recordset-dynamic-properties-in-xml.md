---
title: Propiedades dinámicas de conjuntos de registros en XML
TOCTitle: Recordset dynamic properties in XML
ms:assetid: 6ee1f176-9986-4ade-fc97-e3dad8e6bc6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249439(v=office.15)
ms:contentKeyID: 48545522
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 36069ec0e8e9020bc70ef1ea72ce25f4461c6487
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946961"
---
# <a name="recordset-dynamic-properties-in-xml"></a>Propiedades dinámicas de conjuntos de registros en XML

**Se aplica a**: Access 2013, Office 2013

Las siguientes propiedades de **conjuntos de registros** específicas del proveedor (del Client Cursor Engine) persisten actualmente en el formato XML:

- **AutoRecalc**
- **BatchSize**
- **CommandTimeout**
- **IRowsetChange**
- **IRowsetUpdate**
- **Reshape Name**
- **Resync Command**
- **Unique Catalog**
- **Unique Schema**
- **Unique Table**
- **Update Resync**
- **UpdateCriteria**


Estas propiedades se guardan en la sección de esquema como atributos de la definición de elemento para el **conjunto de registros** que se hace persistente. Estos atributos se definen en el espacio de nombres de esquema del conjunto de filas y deben tener el prefijo "rs:".

## <a name="see-also"></a>Vea también

- [Propiedades dinámicas de ADO](ado-dynamic-properties.md)