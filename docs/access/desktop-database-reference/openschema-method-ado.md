---
title: OpenSchema (método, ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288339"
---
# <a name="openschema-method-ado"></a>OpenSchema (método, ADO)

**Se aplica a:** Access 2013, Office 2013

Obtiene información del esquema de base de datos del proveedor.

## <a name="syntax"></a>Sintaxis

**Establezca* = la*conexión*del juego de registros * * *. OpenSchema (* QueryType *, *criteria*, *SchemaID*)

## <a name="return-values"></a>Valores devueltos

Devuelve un objeto [Recordset](recordset-object-ado.md) que contiene información de esquema. El objeto **Recordset** se abrirá como un cursor estático de solo lectura. El parámetro *QueryType* determina qué columnas aparecen en el objeto **Recordset**.

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*QueryType* |Cualquier valor de [SchemaEnum](schemaenum.md) que represente el tipo de consulta de esquema que se va a ejecutar.|
|*Criteria* |Es opcional. Matriz de restricciones de consulta para cada opción *QueryType*, tal y como se muestra en **SchemaEnum**.|
|*SchemaID* |Identificador GUID de una consulta de esquema del proveedor no definida por la especificación OLE DB. Este parámetro es necesario si el valor de *QueryType* es **adSchemaProviderSpecific**; en caso contrario, no se utiliza.|

## <a name="remarks"></a>Comentarios

El método **OpenSchema** devuelve información autodescriptiva sobre el origen de datos, como qué tablas hay en el origen de datos, las columnas de las tablas y los tipos de datos admitidos.

El argumento de *QueryType* es un identificador GUID que indica las columnas devueltas (esquemas). La especificación OLE DB tiene una lista completa de esquemas.

El argumento de *Criteria* limita los resultados de una consulta de esquema. *Criteria* especifica una matriz de valores que se deben producir en un subconjunto correspondiente de columnas, denominadas *columnas de restricción*, del objeto **Recordset** resultante.

La constante **adSchemaProviderSpecific** se utiliza en el argumento de *QueryType* si el proveedor define sus propias consultas de esquema no estándar además de las anteriormente mencionadas. Cuando se utiliza esta constante, el argumento de *SchemaID* debe pasar el identificador GUID de la consulta de esquema que se va a ejecutar. Si el valor de *QueryType* es **adSchemaProviderSpecific** pero no se proporciona *SchemaID*, se producirá un error.

Los proveedores no tienen que admitir necesariamente todas las consultas de esquema OLE DB estándar. En concreto, la especificación OLE DB sólo requiere **AdSchemaTables**, **adSchemaColumns** y **adSchemaProviderTypes**. Sin embargo, el proveedor no tiene que admitir necesariamente las restricciones de *Criteria* anteriormente mencionadas para esas consultas de esquema.

**Uso del servicio de datos remotos** El método **OpenSchema** no está disponible en un objeto [Connection](connection-object-ado.md) de cliente.

> [!NOTE]
> En Visual Basic, las columnas que tienen un entero sin signo de cuatro bytes (DBTYPE UI4) en el objeto **Recordset** devuelto por el método **OpenSchema** en el objeto **Connection**, no se pueden comparar con otras variables. Para obtener más información sobre los tipos de datos OLE DB, vea el capítulo 13 y el apéndice A de la *Referencia del programador de Microsoft OLE DB*.


