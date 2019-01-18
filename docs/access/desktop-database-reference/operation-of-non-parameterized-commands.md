---
title: Funcionamiento de los comandos sin parámetros
TOCTitle: Operation of non-parameterized commands
ms:assetid: 934740b1-07d0-140e-7c83-00feb34c01d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249651(v=office.15)
ms:contentKeyID: 48546395
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 720cbaf346b64d4d23b1e3314b06ba941e78b700
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701889"
---
# <a name="operation-of-non-parameterized-commands"></a>Funcionamiento de los comandos sin parámetros


**Se aplica a**: Access 2013, Office 2013

Para comandos no parametrizados, durante la ejecución del comando, se ejecutan todos los comandos de proveedor y se crean los **conjuntos de registros**. Si el comando se ejecuta sincrónicamente, todos los **conjuntos de registros** se llenarán completamente. Si se seleccionó un modo de llenado asincrónico, el estado relleno de los **conjuntos de registros** dependerá del modo de llenado y del tamaño de los **conjuntos de registros**.

Por ejemplo, el *comando a principal* podría devolver un **conjunto de registros** de clientes para una compañía desde una tabla Customers y el *comando a secundario* podría devolver un **conjunto de registros** de pedidos para todos los clientes desde una tabla Pedidos.

```vb 
 
SHAPE {SELECT * FROM Customers} 
 APPEND ({SELECT * FROM Orders} AS chapOrders 
 RELATE customerID TO customerID) 
```

Para relaciones principal-secundario no parametrizados, cada objeto **Recordset** principal y secundario debe tener una columna en común para poder asociarlos. Las columnas se mencionan en la cláusula relacionar, *columna primaria* primero y, a continuación, la *columna secundaria*. Las columnas pueden tener nombres distintos en sus objetos **Recordset** respectivos, pero deben hacer referencia a la misma información para poder especificar una relación significativa. Por ejemplo, los objetos **Recordset** de **Customers** y **Orders** podrían tener en común un campo customerID de identificación del cliente. Dado que la pertenencia del **conjunto de registros** secundario se determina mediante el comando del proveedor, el **conjunto de registros** secundario puede contener filas huérfanas. No se puede tener acceso a estas filas huérfanas sin cambiar de forma.

El proceso de forma de datos anexa una columna de capítulo al **conjunto de registros** principal. Los valores de la columna de capítulo son referencias a filas del **conjunto de registros** secundario, que cumplen la cláusula RELATE. Es decir, el mismo valor está en la *columna a principal* de una fila principal determinada y en la *columna a secundaria* de todas las filas del secundario del capítulo. Cuando se utilizan varias cláusulas TO en la misma cláusula RELATE, éstas se combinan implícitamente utilizando un operador AND. Si las columnas principales de la cláusula RELATE no constituyen una clave para el **conjunto de registros** principal, una fila secundaria única podría tener varias filas principales.

Cuando se obtiene acceso a la referencia de la columna de capítulo, ADO recupera automáticamente el **conjunto de registros** representado por la referencia. Tenga en cuenta que, en un comando no parametrizado, aunque se haya recuperado el **conjunto de registros** secundario completo, el capítulo sólo presenta un subconjunto de filas.

Si la columna anexada no tiene ningún *alias de capítulo*, se generará un nombre para ella automáticamente. Un objeto [Field](field-object-ado.md) para la columna se anexará en la colección [Fields](fields-collection-ado.md) del objeto **Recordset**, y su tipo de datos será **adChapter**.

Para obtener información sobre cómo desplazarse por un objeto **Recordset** jerárquico, vea [ Obtener acceso a las filas de un objeto Recordset jerárquico ](accessing-rows-in-a-hierarchical-recordset.md).

