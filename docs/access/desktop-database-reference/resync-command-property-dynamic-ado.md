---
title: Propiedad dinámica Resync Command (ADO)
TOCTitle: Resync Command dynamic property (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa1fe05e6aa7edf04ad74864eb30a03403323c8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306583"
---
# <a name="resync-command-dynamic-property-ado"></a>Propiedad dinámica Resync Command (ADO)

**Se aplica a:** Access 2013, Office 2013

Especifica una cadena de comando proporcionada por el usuario que el método [Resync](resync-method-ado.md) emite para actualizar los datos de la tabla especificada en la propiedad dinámica [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String** que es una cadena de comandos.

## <a name="remarks"></a>Comentarios

El objeto [Recordset](recordset-object-ado.md) es el resultado de una operación JOIN ejecutada en varias tablas base. Las filas afectadas dependen del parámetro *AffectRecords* del método [Resync](resync-method-ado.md). El método **Resync** estándar se ejecuta si las propiedades [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) y **Resync Command** no están establecidas.

La cadena de comandos de la propiedad **Resync Command** es un comando con parámetros o un procedimiento almacenado que identifica de forma exclusiva a la fila que se va a actualizar y que devuelve una única fila que contiene el mismo número de columnas y en el mismo orden que la fila que se va a actualizar. La cadena de comandos contiene un parámetro por cada columna de clave principal de **Unique Table**; de lo contrario, se devuelve un error en tiempo de ejecución. Los parámetros no se rellenan automáticamente con los valores de clave principal de la fila que se va a actualizar.

A continuación se muestran dos ejemplos basados en SQL:

1.  **Recordset** se define mediante un comando:

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    Se establece la propiedad **Resync Command** en:

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    **Unique Table** es *Orders* y la clave principal, *OrderID*, tiene parámetros. La subselección proporciona una forma simple de garantizar mediante programación que se devuelve el mismo número de columnas y en el mismo orden que con el comando original.

2. **Recordset** es definido por un procedimiento almacenado:

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    El método **Resync** debe ejecutar el siguiente procedimiento almacenado:

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    Se establece la propiedad **Resync Command** en:

    `"{call CustordersResync (?)}"`

Una vez más, **Unique Table** es *Orders* y la clave principal, *OrderID*, tiene parámetros.

**Resync Command** es una propiedad dinámica que se anexa a la colección [Properties](properties-collection-ado.md) del objeto **Recordset** cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.

