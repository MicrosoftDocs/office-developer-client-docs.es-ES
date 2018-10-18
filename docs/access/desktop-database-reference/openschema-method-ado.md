---
title: OpenSchema (método, ADO)
TOCTitle: OpenSchema Method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddd823baf153ebc78fc34ca838184f415edd29ef
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605922"
---
# <a name="openschema-method-ado"></a>OpenSchema (método, ADO)


**Se aplica a**: Access 2013 | Office 2013


Obtiene información del esquema de base de datos del proveedor.

## <a name="syntax"></a>Sintaxis

**Establecer *** recordset* = *conexión*. OpenSchema (* QueryType *, *criterios*, *SchemaID*)

<<<<<<< HEAD
## <a name="return-values"></a>Valores devueltos
=======
## <a name="return-values"></a>Valores devueltos
>>>>>>> master

Devuelve un objeto [Recordset](recordset-object-ado.md) que contiene información de esquema. El objeto **Recordset** se abrirá como un cursor estático de solo lectura. El *QueryType* determina qué columnas aparecen en el **conjunto de registros**.

## <a name="parameters"></a>Parámetros

  - *QueryType*

  - Cualquier valor de [SchemaEnum](schemaenum.md) que represente el tipo de consulta de esquema que se va a ejecutar.

  - *Criteria*

  - Es opcional. Una matriz de restricciones de consulta para cada opción *QueryType* , tal y como se muestra en **SchemaEnum**.

  - *SchemaID*

  - Identificador GUID de una consulta de esquema del proveedor no definida por la especificación OLE DB. Este parámetro es necesario si el valor de *QueryType* es **adSchemaProviderSpecific**; de lo contrario, no se usa.

## <a name="remarks"></a>Comentarios

El método **OpenSchema** devuelve información autodescriptiva sobre el origen de datos, como qué tablas hay en el origen de datos, las columnas de las tablas y los tipos de datos admitidos.

El argumento de *QueryType* es un GUID que indica las columnas devueltas (esquemas). La especificación OLE DB tiene una lista completa de esquemas.

El argumento de *Criteria* limita los resultados de una consulta de esquema. *Criteria* especifica una matriz de valores que se deben producir en un subconjunto correspondiente de columnas, denominadas *columnas de restricción*, del objeto **Recordset** resultante.

La constante **adSchemaProviderSpecific** se utiliza para el argumento de *QueryType* si el proveedor define sus propias consultas de esquema no estándar fuera de las anteriormente mencionadas. Cuando se utiliza esta constante, se requiere el argumento de *SchemaID debe* pasar el identificador GUID de la consulta de esquema para ejecutar. Si *QueryType* es **adSchemaProviderSpecific** pero no se proporciona *SchemaID* , se producirá un error.

Los proveedores no tienen que admitir necesariamente todas las consultas de esquema OLE DB estándar. En concreto, la especificación OLE DB sólo requiere **AdSchemaTables**, **adSchemaColumns** y **adSchemaProviderTypes**. Sin embargo, el proveedor no es necesario para admitir las restricciones de *Criteria* mencionadas para esas consultas de esquema.

**Uso de servicio de datos remotos** El método **OpenSchema** no está disponible en un objeto de [conexión](connection-object-ado.md) de cliente.


> [!NOTE]
> <P>En Visual Basic, las columnas que tienen un entero sin signo de cuatro bytes (DBTYPE UI4) en el objeto <STRONG>Recordset</STRONG> devuelto por el método <STRONG>OpenSchema</STRONG> en el objeto <STRONG>Connection</STRONG>, no se pueden comparar con otras variables. Para obtener más información sobre los tipos de datos OLE DB, vea el capítulo 13 y el apéndice A de la <EM>Referencia del programador de Microsoft OLE DB</EM>.</P>


